# rinoOS — live like rino

> a personal portfolio disguised as a desktop operating system. built entirely in one HTML file.

---

## why

the mission was simple: build a personal website. i didn't want to make the usual thing. a page with my name, a list of projects, some links. that's boring and nobody actually reads it.

i wanted something where you have to explore to find out who i am. so instead of a website *about* me, i made an OS that *feels* like mine.

---

## what it is

vanilla JS. no frameworks. no libraries. no backend. one HTML file.

you boot in, pick a wallpaper, land on a desktop, and click around to find out who rino is. every window, every command, every little detail is intentional.

---

## what you can do

**boot**
watch the OS start up with real `[ OK ]` style system messages and a progress bar

**wallpaper picker**
choose from 8 terminal-themed patterns — scanlines, matrix rain, grid, dot matrix, noise, indigo fog, diagonal, pure black

**desktop apps**
open from the dock: about, projects, skills, f1, notes, terminal, contact

**window management**
drag, resize, minimize, maximize — works like a real OS. minimized windows go into a tray next to the dock, click a tile to restore

**right-click menu**
right click the empty desktop for quick shortcuts

**jarvis terminal**
the built-in terminal runs real commands:

```
neofetch
whoami
ls
cat about.txt
sudo make me a sandwich
matrix
hey jarvis, open projects
hey jarvis, help
hey jarvis, close all
hey jarvis, what time is it
```

**sticky notes**
write whatever you want in the notes app

**README app**
open the guide icon in the dock if you get lost

---

## design

**palette**
- `#0D0F1A` — deep navy base
- `#6C63FF` — flat indigo accent
- `#F0EBE1` — warm cream text
- `#8B8FA8` — slate for secondary text
- `#E8957A` — rose for warnings

**typography**
- Cabinet Grotesk — display, headings, body
- DM Mono — terminal output, file paths, code labels only

**icons**
flat purple SVG strokes. no emojis, no gradients.

---

## what was actually hard

**drag vs resize**
both needed `mousemove` on the document. they fought each other until i put them into a single shared handler with two separate state objects — `dragState` and `resizeState`. one wins, one idles.

**the guide hint bubble**
was pointing to the completely wrong spot. a CSS `transform` on the dock silently breaks `position: fixed` for anything nested inside it. had to move the element out of the dock container entirely and calculate its position from the icon's real bounding box on every render.

**the boot progress bar**
looked choppy even when the math was right. `setInterval` with random increments was the culprit — rewrote it with `requestAnimationFrame` and actual elapsed time against a fixed duration. smooth ever since.

---

## what i'm proud of

it actually feels like an OS and not a webpage.

the boot sequence, wallpaper picker, minimized window tray, guide app, resize handles, right-click menu, jarvis terminal — none of that was in a brief. i just kept adding things until it felt done.

---