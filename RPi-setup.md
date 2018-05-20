
This is how to set up a Raspberry Pi to execute via the Movidius NCS.

Note that you will not use the Full SDK, only the API. 
This means that you cannot **develop Graphs** on the Pi, 
only execute ones you have already developed.

You can see an introduction at [https://ncsforum.movidius.com/discussion/670/caffe-build-error-during-ncsdk-installation]

But the simplest build steps are at [https://movidius.github.io/blog/ncs-apps-on-rpi/]

see more at https://medium.com/@hsheil/movidius-neural-compute-stick-and-raspberry-3-quick-start-guide-a89ff5e1d7ca or [https://www.pyimagesearch.com/2018/02/12/getting-started-with-the-intel-movidius-neural-compute-stick/] 
or [https://www.pyimagesearch.com/2018/02/19/real-time-object-detection-on-the-raspberry-pi-with-the-movidius-ncs/] or []


    coming soon

## Cheating on Mac

I wanted to have instructions for setting up a Raspbian image from a macOS, 
but I got lazy. I just passed through the USB device for my microSD card reader, 
abd then followed the instuctions at [https://github.com/artmg/MuGammaPi/wiki/Raspbian-basics] 
with the linked commands at [https://github.com/artmg/lubuild/blob/master/help/configure/write-Distro-to-flash.md#choice--simpler---dd]. 


## Notes on Power Consumption

Movidius say their package runs on less than a watt, 
which we can assume means up to a watt (1W = 1000mW). 
Considering that the Pi draws 200-500mW, 
you would do well to look for a 2W power source for any setup 
where you use the Pi with an NCS. 

## More on Pi

As an alternative to NCS + Pi why not consider 
Google AIY `VisionBonnet` addon for the Pi Zero 
for your project builds. 
It should slim things down and reduce power consumption.
Hopefully coming soon!
[https://www.raspberrypi.org/magpi/aiy-projects-vision-kit/]

