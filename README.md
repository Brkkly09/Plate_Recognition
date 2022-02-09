# Plate_Recognition
Real Time Plate Recognition on Raspberry Pi

Here we use the OpenCV library to detect and recognize number plates, and the Tesseract library is used to read the characters. So before proceeding further, first install the OpenCV, Tesseract, and other required libraries.

Dependency installation process for Raspberry Pi Model 3B+ with Buster

You can download "Raspbian" (Raspberry Pi OS (Legacy) with desktop) for your Raspberry Pi in this link;
https://downloads.raspberrypi.org/raspios_oldstable_armhf/images/raspios_oldstable_armhf-2022-01-28/2022-01-28-raspios-buster-armhf.zip

Installation Phase,

In case, the memory is limited in the Raspberry Pi, run the following commands to uninstall LibreOffice and Wolfram which will not be used.

sudo apt-get purge wolfram-engine libreoffice* scratch -y
sudo apt-get clean & autoremove
