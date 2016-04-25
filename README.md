# eyeBlinkBehaviour

All codes related to Arduino programming and data saving for the Eye-Blink
Conditioning Tasks

To build and upload to arduino   

    $ make 
    $ make upload 

# What to change

The source code goes into `src` folder. Open the makefile and changes the values
of `LOCAL_INO_SRCS` (there should be one or zero `.ino` file). 

Most of source file would have either extension `.cpp` or `.c`. Append them to
variable `LOCAL_CPP_SRCS`. For example, the example project has the following:

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


