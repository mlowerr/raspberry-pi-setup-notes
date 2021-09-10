Notes on setting up a VNC Server on 5.10.60-2-MANJARO-ARM

1. Install tigervnc

```
sudo pacman -S tigervnc
```

2.  Set a VNC password with `vncpasswd`

3.  Start an instance of x0vncserver that will mirror the existing desktop:

```
x0vncserver -display :0 -PasswordFile /home/<user>/.vnc/passwd
```

4.  To make this start automatically I turned step 3's command into a a script (remember to `chmod +x`) and then fro the GUI launch `Session and Startup > Application Autostart` and create a new entry for the script.

Connecting

I use [VNC Viewer](https://www.realvnc.com/en/connect/download/viewer/) to connect.  The connection string to use is `<ip address | hostmame>:5900`

Reference

This was pieced together in using the following as reference not realizing that `x0vncserver` is what I wanted:

https://tigervnc.org/doc/x0vncserver.html
https://www.fosslinux.com/2264/how-to-add-startup-programs-in-manjaro-linux-17.htm

https://archived.forum.manjaro.org/t/setup-vnc-server-in-manjaro/65960/8

https://forum.manjaro.org/t/how-to-set-up-vnc-on-home-network-manjaro-i3/25854

https://forum.manjaro.org/t/how-to-set-up-vnc-on-home-network-manjaro-i3/25854/11

https://mirrors.xtom.com/osdn//storage/g/m/ma/manjaro/Manjaro-User-Guide.pdf