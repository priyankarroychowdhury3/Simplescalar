# Simplescalar
The repository contains the link to source codes required for running the simulator and instructions how to install and run it.

Link of the source code: https://drive.google.com/drive/folders/0B3wnla-WHMXiTWpEMGJGUGJKdkU?usp=sharing

Installation Instructions:

1) Download the source codes: simplesim3, simpletools and simpleutils from the Google Drive Repository.

2) Make a directory called "simplescalar" in your local machine.

3) Within that make a directory called "build" where you have to place the source codes.

4) Place the "example" directory in "simplescalar" directory outside build.

5) Make sure you have the following packages installed on your system: flex, bison, build-essential

6) Now type: 
export PATH=$PATH:/path.../simplescalar/bin
export PATH=$PATH:/path../simplescalar/simplesim-3.0

7) Now lets set up the environment:
Find out the machine hardware name by running the following command on the terminal: uname -m 
Use this to set the HOST environment variable as i686-pc-linux or i386-pc-linux etc. Even if you have a 64 bit machine (machine name x86_64) use i686 itself. We will be using it as 32 bit installation even on the 64 bit machine. 
Now set the following three environmental variables: 
export HOST=FROM_ABOVE_OPTION
export IDIR=<Installation_directory_for_simplescalar>
export TARGET=sslittle-na-sstrix

8) Installing simpleutils:
Unpack the package by using this command: tar xzvf simpleutils-990811.tar.gz
cd simpleutils-990811
Now one change in the code needs to be done:
In the file ld/ldlex.l change all occurrences of yy_current_buffer with YY_CURRENT_BUFFER
Install using following commands:
./configure -host=$HOST -target=$TARGET -with-gnu-as -with-gnu-ld -prefix=$IDIR
make
make install

9) Installing simulator:
Unpack the simulator:
cd $IDIR
tar xzvf simplesim-3v0d.tgz
cd simplesim-3.0
make config-pisa
make

10) You have traversed the half-mile now. Lets traverse the last half and complete it. Since simplescalar is old, it is incompatible with current systems. So, to make it work, follow the technique found out by Sebastian which he has posted on Github: https://github.com/sebastian2696/SimpleScalarUbuntu. All credits to Sebastian to help you traverse the last half mile.
