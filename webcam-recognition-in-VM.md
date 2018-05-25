
## Introduction

This project is to recognise images coming from the webcam on a PC, 
using Lubuntu running in a Virtual Machine guest (VM). 
This example refers to Virtual Box options.

## Pass through your webcam

* Start your VM
* In Virtual Box Guest Menu (toolbar) / Devices / Webcams / _\<choose your webcam\>_
* Inside the actual VM's Start Menu / Sounds and Video / guvcview

This will test whether you have successfully passed your webcam into the VM

If guvcviev failed:
* Open terminal
```
sudo apt install -y cheese
```
* Then run
```
cheese
```

## Clone scripts to use

We found https://github.com/gudovskiy/yoloNCS a little complicated, 
so we instead used https://github.com/jincongho/NCS_TinyYolo for the script to 
take the webcam feed and pass it to YOLO

```
mkdir -p ~/CamRecog
cd ~/CamRecog
git clone https://github.com/jincongho/NCS_TinyYolo.git
cd NCS_TinyYolo
make
```

FYI some people seem to store their CAFFE models on Google Drive, 
from which you can't download using the command line, 
so you'll need to do those manually 

