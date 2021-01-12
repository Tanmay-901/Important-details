# Important-details
Specific details/workarounds/troubleshotting things that are faced frequently.  
>refer named folders for topic/event specific details.  
  
### Keyboard not working:  
1. Check for drivers  
2. Check for keyboard settings
3. Check if working in BIOS.
4. If not working in BIOS, there are chances of hardware issue, otherwise if working in bios, issue is with windows.
5. Turn off laptop, unplug each and every type of cable/cord
6. press and hold `fn + S + V` or `S + V` for 60 seconds to release static energy.
7. Try turning on without plugging in the power supply, if it turns on, then energy not released.
8. Plug the `power cable` and try turning on, it should work now, otherwise It's a hardware issue.

### Night light hue(intensity) adjustment in linux:  
`gsettings set org.gnome.settings-daemon.plugins.color night-light-temperature <temperature>`  
* 1000 Lowest value (really red)  
* 4000 Default night light temperature  
* 6500 Default temperature (night light off)  
* 10000 Highest value (really blue)  

### Convert python file to .exe:  
* run command in same directory `pyinstaller --onefile --noconsole filename.py`
    1. pyinstaller should be installed
    2. `--onefile` is used to specify that only one file should be generated
    3. `--noconsole` is used to specify that console should not open when the exe file is run(along with the executable).
