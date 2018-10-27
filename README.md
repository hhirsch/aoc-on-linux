# Age of Conquerors + WK on Linux
## Wine Setup
Set up a fresh 32 bit Wine prefix. Recommended UI for that is Playonlinux.
Install Direct Play, Microsoft Visual C++ 2010 Runtime, Microsoft Visual C++ 2012 Runtime and Microsoft Visual C++ 2013 Runtime to your AoE II Wine prefix with winetricks. Wine mono should auto install when needed and should be enough.

## Install HD
### HD Without Wine (recommended)
- If you enable Steam Play for non-compatible games you can install AoE II through your Linux steam
- Deactivate the Steam overlay for better performance
### HD With Wine
   This method will soon stop working when Steam stops support of Windows XP since the Steam UI is not usable in any other setting.
- Install Play On Linux
- Install Steam inside Play on Linux
- Fix store rendering
    - Set Wine to Windows XP
    - Install MS core fonts
    - Add parameters to steam icon `-no-cef-sandbox -no-dwrite` in playonlinux
- Install AoE if you get connection errors open *drive_c/Program Files/Steam/config/config.vdf* and add [this code](config.vdf) right after "cid" on a new line
- Deactivate the Steam overlay for better performance
### (Optional) Bypass Launcher
The game won't start unless you bypass the launcher.
Go to the game folder (right click and go "open applications directory" then navigate to /steamapps/common/age2HD/ ). 
Rename the Launcher.exe to someting else. 
Then make a copy of the AoK HD.exe and name it Launcher.exe. Having a working HD installation is recommended because it
allows you to set up your hotkeys once and then import them to AoC and WK with the WK installer.
### (Optional) Install Fonts
In order to have the classic look for menus and some messages you need to install the original fonts.
Install the fonts in *drive_c/Program Files/Steam/steamapps/common/Age2HD/resources/_common/fonts* to your system.
## Install Voobly
First install [the compatibility patch](https://www.memberplus.net/) and then create an account on [voobly.com](https://www.voobly.com/) and install voobly.
### Make voobly links work in your browser
Install mimeo and xdg-utils-mimeo. Then open ~/.config/mimeo/associations.txt
and add

```
/usr/share/playonlinux/playonlinux --run \"voobly\" %u
  ^voobly://
```
now you can open voobly links right by clicking the link in your linux browser.

#### Firefox
Go to about:config and right-click. Then click on New->Boolean->network.protocol-handler.expose.voobly -> Value -> false
Upon the next click on a voobly link firefox will ask you to choose a program to open voobly links. Choose xdg-open.
### Optimize Voobly Performance
Follow this guide for [better performance in voobly](https://ageofnotes.com/resolve-issues/age-empires-2-max-performance-windows-10/).
