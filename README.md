# Kernel-upgrade

#!/bin/bash

This script is for the kernel upgrade

#Author Nathan Johnson: 11/21/2017

echo
echo "Downloading the Kernel Version 4.14.8"
echo
sleep 4

wget https://cdn.kernel.org/pub/linux/kernel/v4.x/linux-4.14.8.tar.xz
echo
echo " Extracting the Package"
echo

sleep 2

tar -xvf linux-4.14.8.tar.xz

cd linux-4.14.8
echo
echo "Instaling Dependencies. Please wait...."
echo
yum groupinstall "Development Tools" -y

yum install openss* gcc* ncurses-devel libncurses5-dev -y

make defconfig

make
#This script is for the kernel upgrade
