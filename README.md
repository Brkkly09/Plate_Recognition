# Plate_Recognition
Real Time Plate Recognition on Raspberry Pi

Here we use the OpenCV library to detect and recognize number plates, and the Tesseract library is used to read the characters. So before proceeding further, first install the OpenCV, Tesseract, and other required libraries.

Dependency installation process for Raspberry Pi Model 3B+ with Buster

You can download "Raspbian" (Raspberry Pi OS (Legacy) with desktop) for your Raspberry Pi in this link;
*https://downloads.raspberrypi.org/raspios_oldstable_armhf/images/raspios_oldstable_armhf-2022-01-28/2022-01-28-raspios-buster-armhf.zip*

Installation Phase,

In case, the memory is limited in the Raspberry Pi, run the following commands to uninstall LibreOffice and Wolfram which will not be used.
```
$ sudo apt-get purge wolfram-engine libreoffice* scratch -y
$ sudo apt-get clean & autoremove
```
Update your Pi with the following two commands:
```
$ sudo apt-get update
$ sudo apt-get upgrade
$ sudo rpi-update
$ sudo reboot
````
The next command installs packages required for all the other steps:
````
$ sudo apt-get install build-essential cmake cmake-curses-gui pkg-config
$ sudo apt-get install cmake gfortran
$ sudo apt-get install python3-dev python3-numpy
$ sudo apt-get install libjpeg-dev libtiff-dev libgif-dev
$ sudo apt-get install libavcodec-dev libavformat-dev libswscale-dev
$ sudo apt-get install libgtk2.0-dev libcanberra-gtk*
$ sudo apt-get install libxvidcore-dev libx264-dev libgtk-3-dev
$ sudo apt-get install libtbb2 libtbb-dev libdc1394-22-dev libv4l-dev
$ sudo apt-get install libopenblas-dev libatlas-base-dev libblas-dev
$ sudo apt-get install libjasper-dev liblapack-dev libhdf5-dev
$ sudo apt-get install gcc-arm* protobuf-compiler
$ sudo apt-get install python-dev python-numpy
$ sudo apt-get install autoconf automake libtool libleptonica-dev libicu-dev libpango1.0-dev libcairo2-dev cmake git libgtk2.0-dev pkg-config libavcodec-dev libavformat-dev libswscale-dev python-dev python-numpy libjpeg-dev libpng-dev libtiff-dev libjasper-dev libdc1394-22-dev virtualenvwrapper liblog4cplus-dev libcurl4-openssl-dev libtiff5-dev gcc make ca-certificates autoconf-archive libgstreamer1.0-dev libgstreamer-plugins-base1.0-dev
````
Then:
````
$ sudo apt-get install -y openjdk-8-jdk
$ sudo apt-get install -y default-jdk
$ export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64
````
Then:
````
$ sudo apt install libgtk-3-dev
$ sudo apt-get install libv4l-dev
$ cd /usr/include/linux
$ sudo ln -s ../libv4l1-videodev.h videodev.h
$ cd ~
````
The following commands will download, make and install Leptonica. Leptonica is one of the dependencies of OpenALPR.
````
$ sudo apt-get install libopencv-dev libtesseract-dev git cmake build-essential libleptonica-dev
$ sudo apt-get install liblog4cplus-dev libcurl3-dev
$ sudo apt-get install beanstalkd
````
Then:
````
$ sudo apt-get install libqtgui4
$ sudo apt-get install libqt4-test
````
After that, use the below command to install the OpenCV and on your Raspberry Pi.
````
$ pip3 install opencv-contrib-python==4.1.0.25
````
To install the Tesseract, first, configure the Debian Package (dpkg) using the below command:
````
$ sudo dpkg --configure -a
````
After that, install the Tesseract OCR (Optical Character Recognition) using the apt-get option.
````
$ sudo apt-get install tesseract-ocr
````
After that, install the pytesseract using the pip or pip3.
````
$ pip3 install pytesseract
````
After this, install the PYTTSX3 library for text to speech conversion using the below command:
````
$ pip install pyttsx3
$ pip3 install pyttsx3
````
imutils is used to make essential image processing functions such as translation, rotation, resizing, skeletonization, and displaying Matplotlib images easier with OpenCV. Use the below command to install the imutils:
````
$ pip3 install imutils
$ pip install imutils
````
Then install these libraries using the codes below so that tesseract ocr can be installed correctly.
````
$ sudo apt-get install libleptonica-dev 
$ sudo apt-get install tesseract-ocr tesseract-ocr-dev
$ sudo apt-get install libtesseract-dev
$ pip install tesseract
$ pip install tesseract-ocr
````
# SMTP Mail Setup for Raspberry Pi Car Plate Recognition
SMTP (Simple Mail Transfer Protocol) is the standard protocol for providing email services on a TCP/IP network. This server provides the ability to receive and send email messages. We are using SMTP to send a mail when the Raspberry Pi detects and recognizes a license plate.

To use the SMTP services on Raspberry Pi, we first have to install the SMTP library on Pi. Use the below command to install the same:
````
$ sudo apt-get install ssmtp
````
Now we have to edit the configure file. For that, open Configuration file using the below command:
````
$ sudo nano /etc/ssmtp/ssmtp.conf
````
And add the below lines. Don’t forget to add your email and email password.
````
root=postman
mailhub=smpt.gmail.com:587
AuthUser=Your email IDn@gmail.com
AuthPass=Your email Password
FromLineOverride=YES
UseSTARTTLS=YES
Debug=YES
````
