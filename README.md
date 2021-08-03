
# repl-freeglut-c
C repl.it demo for freeglut OpenGL
```
REPL:   https://repl.it/@qcm/repl-freeglut-c
GITHUB: https://github.com/xp5-org/repl-freeglut-c
```
&nbsp;
&nbsp;
&nbsp;

Use this repl as a template for freeglut OpenGL development in repl

The included script checks if the correct freeglut/GL packages are installed. If the modules are not present, it installs them.

If you edit the fractals.c program and re-run the script, it will re-compile your program and back up the old version in the "backup" folder, versioning it with the current date and time. This will allow you to make live edits and revert on repl without much work.



Fractals.c here -> http://openglut.sourceforge.net/fractals_8c.html











UPDATE: 
06/30/2021:
- this used to work but is now broken since the repl update. im now seeing the "OpenGL GLX extension not supported by display" error

08/03/2021:
- i changed nothing, its working again. 

  

   
    
Sometimes i get the following error after my program closes strangely or if i exit the repl and reopen:
```
===================================================================
Loading main binary 
Starting X
..............................................................FATAL: /usr/bin/polygott-x11-vnc: Gave up waiting for X server :0
Failed to open X11 display; make sure the DISPLAY environment variable is set correctly
script.bash: line 79:   890 Aborted                 (core dumped) $replrootpath/$target_file
done
===================================================================
```
i am not sure how to resolve it, sometimes killing the open xorg sessions resolves, sometimes 
the only way to fix is close repl and wait hours - or an immediate workaround is to FORK the repl 
as the forked repl will inherit a new environment. I need to figure out how to reset X11/Xorgvnc/etc 
at the start of this bash script

if you are getting errors running this the second or third time but worked the first or are getting 
strange behavior - such as windows which should be windowed are now full-screen with no 
option to close  - this can be due to a bad environment on REPL and will need to let the environment 
close and reset after some time passes. or can fork the environment to get a new container.
