# OpenCV Detection with Raspberry Pi 5
This is a project I worked on to demo computer vision on a Raspberry Pi 5. Make sure for this demo that you have:

* [Raspberry Pi Official Camera Module V2](https://www.raspberrypi.com/products/camera-module-v2/) (You can also use the [Raspberry Pi High-Quality Camera](https://www.raspberrypi.com/products/raspberry-pi-high-quality-camera/))
* Micro SD Card 
* [Power Supply](https://www.raspberrypi.com/products/27w-power-supply/)
* Monitor
* HDMI Cord 
* Mouse and Keyboard

Once you have all of the necessary hardware, flash the latest Raspberry Pi 5 OS onto the Micro SD card and boot to the OS. Make sure that you enable your camera in the *Raspberry Pi 5 Configuration* in *Preferences*, then follow these steps:

1) Open a Terminal window and make sure that you are in the ***/home/pi/Desktop*** directory (of course if you named your user something else than ***pi***, use that name instead):

```bash
cd /home/pi/Desktop
```

2) Lets clone this git repository:

```bash
git clone https://github.com/mark-carahan/opencv-rasp5.git
```

3) Make sure that you have the necessary modules installed:

```bash
sudo apt-get update && sudo apt-get upgrade -y
sudo apt-get install python3-opencv
```

4) You can either open Thonny and run ***object-ident.py*** file or from the Terminal window run:

```bash
cd opencv-rasp5
python3 object-ident.py
```

5) This will open a window that shows the what the camera is looking at as well as a green square with the name of the detected object and the confidence score of the detection.

6) There are two more files that do extra processing where it will only show a square around a cup (***object-ident-2.py***) or a cup and a horse (***object-ident-3.py***).

7) You can change these values by going into the ***coco.names*** file and see what else the program can detect.