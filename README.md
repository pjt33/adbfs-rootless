This variant of adbfs workous even WITHOUT having root access (busybox) on your phone!

Instructions:
=============

You will need libfuse-dev. On ubuntu
    
    sudo apt-get install libfuse-dev

Clone the repository 

    git clone git://github.com/spion/adbfs-rootless.git
    cd adbfs-rootless    

Build

    make

Copy the binary adbfs to <path-to-android-sdk>/platform-tools directory. 
If platform-tools is in your $PATH you can skip this step.

Create a mount point if needed (e.g. in your home directory)

    mkdir ~/droid

Before mounting you need to run adb once to make sure that the daemon
is started (will be fixed eventually).

From the sdk's platform-tools dir:

    ./adb shell ls

You can now mount your device (also from the platform-tools dir):

    ./adbfs ~/droid


