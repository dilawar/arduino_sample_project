#  Sample project 

This is a working version of a real lab project (https://github.com/ananthmurthy/eyeBlinkBehaviour).  
This is here for a demo purpose

To build and uploading to arduino  is as simple as typing

    $ make 
    $ make upload 

And you can edit your files in your faviorite editor. Works on Mac and Linux.

# What to change?

The source code goes into `src` folder. Open the makefile and changes the values
of `LOCAL_INO_SRCS` (there should be one or zero `.ino` file in your project). 

Most of source file would have either extension `.cpp` or `.c`. Append them to
variable `LOCAL_CPP_SRCS`. For example, this sample project has the following:

~~~~
## INO file and other cpp files
LOCAL_INO_SRCS     = $(PROJECT_DIR)/src/eye_blink_main.ino 
LOCAL_CPP_SRCS     = $(PROJECT_DIR)/src/TriggerImaging.cpp \
		$(PROJECT_DIR)/src/Solenoid.cpp \
		$(PROJECT_DIR)/src/PhaseChangeRoutine.cpp \
		$(PROJECT_DIR)/src/main.cpp \
		$(PROJECT_DIR)/src/LocalLibrary.cpp \
		$(PROJECT_DIR)/src/LCDRelated.cpp \
		$(PROJECT_DIR)/src/Initialize.cpp \
		$(PROJECT_DIR)/src/DetectBlinks.cpp \
		$(PROJECT_DIR)/src/Globals.cpp \
		$(PROJECT_DIR)/src/ChangePhase.cpp 


~~~~

You don't have to change anything else. I've tested is on `Mac` and `Linux`.
Of-course you need to install arduino. Even if you don't have a board to connect
to, you can still build your project.




[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/dilawar/arduino_sample_project/trend.png)](https://bitdeli.com/free "Bitdeli Badge")

