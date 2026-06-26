<<<<<<< HEAD
# rinoOS - live like rino

This started as a simple assignment: build a personal website.

I didn't want to make the typical portfolio with my name, a list of projects, and some links. That's not really fun to look through, and it doesn't tell you much about who I am. Instead, I built something people have to explore.

**Live Like Rino** is a personal portfolio disguised as a desktop operating system. You boot into a startup screen, choose a wallpaper, and land on a desktop where every app, window, and interaction reveals a little more about me.

Everything is built in a **single HTML file** using only HTML, CSS, and vanilla JavaScript—no frameworks, libraries, or backend.

### What you can do

* Watch the OS boot up before entering the desktop.
* Choose from 8 wallpapers.
* Open apps from the dock.
* Drag, resize, minimize, maximize, and close windows.
* Right-click the desktop for shortcuts.
* Read the built-in guide if you get lost.
* Write in the Sticky Notes app.
* Talk to the JARVIS terminal with commands like:

  ```
  hey jarvis, help
  hey jarvis, open projects
  ```

### Things that were harder than they looked

Most of the challenge came from small details.

Getting dragging and resizing to work nicely together took a lot of trial and error. One bug had the guide bubble pointing to completely the wrong place because a CSS `transform` on the dock changed how `position: fixed` behaved. The boot animation also looked surprisingly choppy, so I rewrote it using `requestAnimationFrame` with real elapsed time instead of relying on `setInterval`.

### My favorite part

It actually feels like an operating system instead of a webpage.

The boot sequence, wallpaper picker, minimized window tray, interactive guide, and JARVIS terminal weren't required for the assignment—I just kept adding features until it felt complete.

If you're checking it out, let it boot, pick a wallpaper, click around the dock, right-click the desktop, and definitely try the terminal.
=======
# rinoOS — live like rino

the mission was simple: build a personal website.
i didn't want to make the usual thing. a page with my name, a list of projects, some links. that's boring and nobody actually reads it. i wanted something where you have to explore to find out who i am.
so instead of a website about me, i made an OS that feels like mine.

what it is:
a personal portfolio disguised as a desktop operating system. you boot in, pick a wallpaper, land on a desktop, and click around to find out who rino is. every window, every command, every little detail is intentional.
built entirely in a single HTML file. vanilla JS, no frameworks, no libraries, no backend.

what you can do:

watch the OS boot with real [  OK  ] style system messages
pick from 8 terminal-themed wallpapers (scanlines, matrix rain, grid, noise, and more)
open apps from the dock — about, projects, skills, f1, notes, terminal, contact
drag, resize, minimize, and maximize windows
minimize windows into a tray next to the dock, restore them by clicking the tile
right click the empty desktop for shortcuts
open the README app if you get lost
write in the sticky notes app
use the jarvis terminal with real commands:

neofetch
whoami
ls
cat about.txt
sudo make me a sandwich
matrix
hey jarvis, open projects
hey jarvis, help

what was actually hard:
most of the challenge came from details that looked small and weren't.
drag and resize fought each other until i consolidated them into one shared mouse event handler. the guide bubble was pointing to completely the wrong spot because a CSS transform on the dock silently broke position: fixed for anything inside it — had to move the element out of that container entirely and calculate the position from the icon's real bounding box. the boot bar looked choppy even when the math was right, rewrote it with requestAnimationFrame and real elapsed time instead of setInterval random increments.

what i'm proud of:
it actually feels like an OS and not a webpage.
the boot sequence, wallpaper picker, minimized window tray, guide app, resize handles, right click menu, jarvis terminal — none of that was in the brief. i just kept adding things until it felt done.

let it boot. pick a wallpaper. type neofetch in the terminal.
>>>>>>> f77dbd4 (css rework)
