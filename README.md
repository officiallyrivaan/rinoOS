rinoOS — live like rino

why:

i didn't want to make the usual thing. name at the top, list of projects, some links, call it a day. nobody actually reads those.

i wanted something you had to explore. so instead of a page about me, i made an OS that feels like mine.

what it is:

vanilla JS. no frameworks. no libraries. no backend. one file.

you boot in, pick a wallpaper, land on a desktop, and click around. every window, every command, every little detail is intentional.

what you can do:

boot
watch the OS start with real [ OK ] style messages and a progress bar

wallpaper picker
8 terminal-themed patterns — scanlines, matrix rain, grid, dot matrix, noise, indigo fog, diagonal, pure black

desktop apps
open from the dock: about, projects, skills, f1, notes, terminal, contact

window management
drag, resize, minimize, maximize. minimized windows go into a tray next to the dock. click a tile to restore.

right-click menu
right click the empty desktop for shortcuts

jarvis terminal
built-in terminal. real commands:

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

sticky notes
write whatever in the notes app

README app
there's a guide icon in the dock if you get lost

design:

palette


#0D0F1A — deep navy base
#6C63FF — flat indigo accent
#F0EBE1 — warm cream text
#8B8FA8 — slate for secondary text
#E8957A — rose for warnings


typography


Cabinet Grotesk — display, headings, body
DM Mono — terminal output, file paths, code labels only


icons
flat purple SVG strokes. no emojis, no gradients.

what was actually hard:

drag vs resize
both need mousemove on the document. they kept fighting each other. fixed it by putting everything into one shared handler with two separate state objects — dragState and resizeState. one wins, one idles.

the guide hint bubble
was pointing to completely the wrong spot. a CSS transform on the dock silently breaks position: fixed for anything inside it. had to pull the element out of the dock entirely and calculate position from the icon's real bounding box.

the boot progress bar
looked choppy even when the math was right. setInterval with random increments was the problem — rewrote it with requestAnimationFrame and actual elapsed time against a fixed duration. smooth now.

what i'm proud of:

it actually feels like an OS and not a webpage.

the boot sequence, wallpaper picker, minimized tray, guide app, resize handles, right-click menu, jarvis terminal — none of that was in a brief. i just kept adding things until it felt done.