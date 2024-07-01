# MacIssues

- Mouse acceleration cannot be turned off
  - Note: Maybe it's turned off when the speed is set to lowest, but it's unusable at that setting, at least with a mouse with around 2000dpi.
  - Solution: https://triq.net/mac/mouse-acceleration (System Settings apps might have to be started after restart to work, needs testing.)

- Home/end button does not move cursor to start/end of line, instead it moves page to top/bottomm.
  - Note: shortcut override (eg. with BTT) does not work consistently and terminal needs additional steps.
  - Solution: https://damieng.com/blog/2015/04/24/make-home-end-keys-behave-like-windows-on-mac-os-x/
  - Additional steps for terminal: https://jeffmikels.org/posts/how-to-fix-home-and-end-keys-in-the-mac-terminal/
  - Note: In case one line is wrapped to multiple lines, end/home will move the cursor to the very beginning or end. This is in contrast to Windows behavior and seems less practical. But arrow keys works as expected for wrapped single lines.

- Application switcher (Alt-Tab on Windows) has several issues
  - I have Command and Option key switched for muscle memory reasons. At least in this case the app switcher shortcut on external keyboard is Ctrl+Tab instead of Alt+Tab.
  - Application switcher UI does not consistently appear on primary display, and even that would be a limitation. It would be logical to be on the currently active screen.
  - There's no thumbnail preview of the application windows. In fact all windows appear as one, regardless of whether those are on the same or separare displays. There's no way to switch between the windows of an application with this UI.
  - Solution: brew install --cask alt-tab

- F5 not working in Chrome
  - Solution: https://www.coolfundas.com/set-f5-shortcut-to-refresh-chrome-browser-mac/
  - Note: This will not work in DevTools window.

- MacOS dock is very limited
  - Does not support multiple windows
  - Does not support thumbnail preview
  - Not space efficient: Although the height is configurable it takes up more space then a Windows/Linux taskbar, because it contains only icons, while other solutions contains mainly text and additionally a small icon.
  - Active applications and the number of windows of windows are not easily visible at first glance. The dots that indicates the active applications are not a sufficient way to indicate that.
  - Solution: **no solution**. There are no alternative docks or ways to extend the default dock that are of acceptable quality.
  - Note: A possible workaround is to hide the Dock and use Alt Tab only.

- Scroll direction is the same on the integrated touchpad and an external mouse
  - Note: Inverted scrolling (natural scrolling) is preferred on modern touchpads, but then an external mouses wheel will be reversed.
  - Solution: https://github.com/noah-nuebling/mac-mouse-fix
  - Note for solution: the solution adds some extra modifications for the mouse buttons, which eg. makes the middle button hold free scroll impossible. Since the solution is open source this could be fixed with a pull request.

- Hungarian keyboard layout is wrong
  - Note: some symbol characters, eg. parenthesis are on wrong places.
  - Solution: https://github.com/zaki/mac-hun-keyboard

- There's no Total Commander
  - Solution: https://mac.eltima.com/file-manager.html
  - Note: this is quite limited compared to Total Commander.

- There's no simple plain text editor
  - Solution: http://www.barebones.com/products/bbedit/
  - Note: this is quite limited compared to Notepad++. An alternative is to just use VS Code.

- No easy way to maximize/restore a window (not full screen)
  - Note: Double click on title bar sometimes work but is not consistent.
  - Solution: BetterTouchTool (BTT) out of the box supports snapping to top and both sides to maximize and half-fill the screen like in Windows.
  - Note: After a window has been maximized by snapping to top it can be restored by dragging it down. But more testing is needed to check whether this is consistent.
  - Note: I experimented with another solution that repurposes the green full screen button as a maximize/restore button, but currently it's not consistent. Some info can be found here: https://community.folivora.ai/t/get-active-window-size-and-screen-size/29735/10

- 3 finger tap/click on touchpad is not handled as middle mouse click
  - Note: Mostly useful for opening links in new tab in Chromium-based browsers
  - Solution: Remap with BTT
  - Note: 3 finger tap is not consistent. 3 finger click is better, but more experience is needed to tell if 100% consistent.

- No shortcut for Activity Monitor
  - Solution: Create in BTT

- No screenshot snapping tool, complicated shortcuts for screenshots and no support for PrtScr button
  - Solution: BTT support multiple ways to create snapshots. You can select region for snapshot and edit it immediately.

- Applications with no open windows sometimes keeps running for no reason
  - Note: In some cases it makes sense for an application to keep running background tasks, but it's possible to do without showing up in the running applications (eg. on the Dock). There's no good reason to be in this half-opened state.
  - Solution: On the AltTab user interface there's a purple quit button wihich is a convinient way to close these apps.
  - Alternative solution: There are tools to do this and BTT can also do it, but sometimes the detection for windowless apps fail and important windows are closed immediately after they open. These can cause weird behavior and issues. My suggestion is to use AltTab, it's convenient.

- It's not possible to set volume for each application
  - Solution: https://github.com/kyleneideck/BackgroundMusic

- There's no paint program
  - Solution: https://sourceforge.net/projects/paintbrush/
  - Note: Further testing is needed to evaluate the usability of this.

- No support for android usb tethering
  - Solution: https://github.com/jwise/HoRNDIS

- You don't receive notification from certain apps
  - Note: Notifications for each app are always disabled by default. But when you first launch the app macOS shows a popup where you can enable the notifications. Sometimes this notification either does not appear or get's discarded by another one.
  - Solution: Check notification settings in System Settings after every app install or when you suspect that notifications are missing.

- Sound settings gets disabled sometimes when using an HDMI monitor, especially volume control on the connection external monitor.
  - This one requires more testing, the scope is not clear yet.
  - Potential sultion and infos: https://github.com/dragstor/mac-sound-fix

- There's no option to completely disable drag lock
  - Note: There's a 500-1000ms delay even when "without drag-lock" is selected.
  - Solution: https://github.com/ideawu/Mac-No-Drag-Release-Delay
  - Note: Solution link does not have a binary anymore, only source code. I added a binary to this repo but it's from a very old forum post.

- Very slow key repeate rate
  - Solution: Simple for this one, set it all the way up in System Settings -> Keyboard.

- Mac modifier keys are on different places by functionality then standard PC modifier keys
  - Note: This makes it hard to switch between macOS and other OSes due to muscle memory.
  - Solution: At least on Macbook Pro 14" M1 the following setup makes the modifier key layout consistent between the laptop, external keyboards and other OSes:
    - On laptop set fn (globe) to command, option to fn, command to option. Effective keys from left to right: command, control, fn, option.
    - On external keyboard set control to command and command to control. Effective keys from left to right: command, control, option.

- Cannot quickly view images in a directory
  - Note: Preview app does not allow navigating between images in a directory. It allows opening multiple images, but that's not suitable for directories that contains not just images. Quick View might be an alternative. But it's reasonable to have a small program that can show an image and navigate between the images with the arrow keys.
  - Solution: https://github.com/lambdan/imageviewer5

- Mouse cursor wiggles when laptop is docked
  - Context: https://www.reddit.com/r/MacOS/comments/16y4rbn/mouse_cursor_wiggling_on_external_screen_only_mbp/
  - Solution: **no solution**
