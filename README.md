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
