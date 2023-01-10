# MacIssues

- Mouse acceleration cannot be turned off
  - Note: Maybe it's turned off when the speed is set to lowest, but it's unusable at that setting, at least with a mouse with around 2000dpi.
  - Solution: https://triq.net/mac/mouse-acceleration (System Settings apps might have to be started after restart to work, needs testing.)

- Home/end button does not move cursor to start/end of line, instead it moves page to top/bottomm.
  - Note: shortcut override (eg. with BTT) does not work consistently and terminal needs additional steps.
  - Solution: https://damieng.com/blog/2015/04/24/make-home-end-keys-behave-like-windows-on-mac-os-x/
  - Additional steps for terminal: https://jeffmikels.org/posts/how-to-fix-home-and-end-keys-in-the-mac-terminal/

- Application switcher (Alt-Tab on Windows) has several issues
  - I have Command and Option key switched for muscle memory reasons. At least in this case the app switcher shortcut on external keyboard is Ctrl+Tab instead of Alt+Tab.
  - Application switcher UI does not consistently appear on primary display, and even that would be a limitation. It would be logical to be on the currently active screen.
  - There's no thumbnail preview of the application windows. In fact all windows appear as one, regardless of whether those are on the same or separare displays. There's no way to switch between the windows of an application with this UI.
  - Solution: brew install --cask alt-tab

- F5 not working in Chrome
  - Solution: https://www.coolfundas.com/set-f5-shortcut-to-refresh-chrome-browser-mac/
