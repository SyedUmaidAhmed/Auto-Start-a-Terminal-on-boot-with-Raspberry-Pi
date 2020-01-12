# Auto-Start-a-Terminal-with-Script-on-boot-with-Raspberry-Pi
This process will help in starting a terminal on boot with Raspberry Pi Microcomputers


When you edit or create autostart file in your user space like

                  
                      ~/.config/lxsession/LXDE-pi/autostart


then, this file will override global lxsession autostart file in

                      /etc/xdg/lxsession/LXDE-pi/autostart
                      
                      
so you should copy everything from global file to your newly created file. By this way , after reboot you won't get a blank screen running openbox.

So, your file should contain

@lxpanel --profile LXDE-pi
@pcmanfm --desktop --profile LXDE-pi
@xscreensaver -no-splash
point-rpi
And then add your necessary startup items at the bottom like

                          @lxterminal

Press Ctrl + X and then Yes. This will save your file. Try sudo reboot on your terminal. On startup you will automatically find a terminal on the screen.

If you want your GUI based python scripts to run in automode when the terminal started please check this link and follow the guide of the answer which is voted for 199 (The nanoscript thing ... etc)

Link to follow ro execute script of python in auto-mode with terminal:

            https://raspberrypi.stackexchange.com/questions/8734/execute-script-on-start-up

