rinoOS — Live like rino

reasons why:

I didn't want to create another usual website. A logo, a list of my projects, a couple of links, goodnight. No one actually reads that crap.

I wanted something that should be explored. That's why I created my OS instead of a boring page about myself.

about this project:

vanilla JS. no frameworks. no libraries. no backend. one file.

you boot up the OS, choose your wallpaper, get to a desktop and browse around. Everything, every single element was thought through.

what you can do with it:

watch the OS booting up with actual [ OK ] style messages and progress bar

wallpaper picker 8 wallpaper designs inspired by terminals: scanlines, matrix rain, grid, dot matrix, noise, indigo fog, diagonals, pure black

apps on a desktop all the apps appear when you launch the OS and can be opened from the dock: about, projects, skills, f1, notes, terminal, contact

windows manager drag, resize, minimize and maximize windows. minimized windows are stored in a tray near the dock, just click the tile to return to your app.

right-click menu right click the empty desktop for shortcuts

jarvis terminal terminal that comes pre-installed in jarvis. real commands:

neofetch whoami ls cat about.txt sudo make me a sandwich matrix hey jarvis, open projects hey jarvis, help hey jarvis, close all hey jarvis, what time is it

sticky notes write whatever you like in the sticky notes application

README app you can find an icon that represents a guide in the dock

design:

palette

#0D0F1A — deep navy base color #6C63FF — flat indigo accent #F0EBE1 — cream text #8B8FA8 — slate color for secondary text #E8957A — rose for warnings

typography

Cabinet Grotesk — display, headings, body DM Mono — terminal output, file paths, code labels only

icons flat purple SVG strokes. no emojis, no gradients.

difficulties:

drag & resize both events use mousemove event listener on the whole document. they were conflicting with each other. solved by creating one handler with two state objects inside — dragState & resizeState. one takes place and another waits.

The hint bubble on the guide was pointing to an area that was totally off. A CSS transform on the dock quietly made the position:fixed property break for any child elements. It turned out I had to remove the element from the dock itself and use its actual bounding box to compute the position.

The boot progress bar seemed to be jerky despite correct math calculations. The culprit turned out to be setInterval with randomized incrementations. Rewrote it using requestAnimationFrame and actual elapsed time relative to a fixed duration.