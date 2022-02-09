# Plate_Recognition
Real Time Plate Recognition on Raspberry Pi
Installation Phase

$ sudo apt-get update
$ sudo apt-get upgrade
$ sudo rpi-update
$ sudo reboot

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
$ sudo apt-get install -y openjdk-8-jdk
$ sudo apt-get install -y default-jdk
$ export JAVA_HOME=/usr/lib/jvm/java-8-openjdk-amd64

$ sudo apt install libgtk-3-dev
$ sudo apt-get install libv4l-dev
$ cd /usr/include/linux
$ sudo ln -s ../libv4l1-videodev.h videodev.h
$ cd ~

$ sudo apt-get install libopencv-dev libtesseract-dev git cmake build-essential libleptonica-dev
$ sudo apt-get install liblog4cplus-dev libcurl3-dev
$ sudo apt-get install beanstalkd

$ sudo apt-get install libqtgui4
$ sudo apt-get install libqt4-test

$ pip3 install opencv-contrib-python==4.1.0.25
$ sudo dpkg --configure -a
$ sudo apt-get install tesseract-ocr
$ pip3 install pytesseract
$ pip install pyttsx3
$ pip3 install pyttsx3
$ pip3 install imutils
$ pip install imutils

$ sudo apt-get install libleptonica-dev 
$ sudo apt-get install tesseract-ocr tesseract-ocr-dev
$ sudo apt-get install libtesseract-dev
$ pip install tesseract
$ pip install tesseract-ocr

$ sudo apt-get install ssmtp
$ sudo nano /etc/ssmtp/ssmtp.conf

root=postman
mailhub=smpt.gmail.com:587
AuthUser=Email ID
AuthPass=Email Password
FromLineOverride=YES
UseSTARTTLS=YES
Debug=YES
