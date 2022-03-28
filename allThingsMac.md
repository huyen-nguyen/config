- **Disable Notification Red Dot on Mac** ([answer from apple.stackexchange](https://apple.stackexchange.com/a/344279/450143))

      defaults write com.apple.systempreferences AttentionPrefBundleIDs 0

- **Clock on menu bar shown in gray, transparent-ish** ([answer from r/MacOS](https://www.reddit.com/r/MacOS/comments/kfuycs/macos_111_bug_the_clock_in_the_status_bar_is/))
    - That happens when you enable Do Not Disturb. Option-click the time to toggle it.

        - If you add the DND menu to the menu bar (System Preferences / Dock & Menu Bar / Do Not Disturb), it will not gray out the clock like that when DND is on.

    - If you don't want to see the icon on menu bar, you can check the box for Focus to `Show in Menu Bar` (-> Clock shown in clear) then uncheck that box. The clock remains clear, but the icon is gone. However this setting will be lost upon restart/shutdown.

- **CPU temperature**

      sudo powermetrics --samplers smc -i1 -n1

- **Install 7zip** ([answer from superuser](https://superuser.com/a/667076/988063))

   First update your brew to be sure you are getting the latest p7zip
      
      brew update
      
   Use Homebrew to install p7zip:

      brew install p7zip
      
   Add all files in the `coffee` directory to the compressed file `press.7z`:

      7z a press.7z coffee

   Unzip `press.7z`:

      7z x press.7z
