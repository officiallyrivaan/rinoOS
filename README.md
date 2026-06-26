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
