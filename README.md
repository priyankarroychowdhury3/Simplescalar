# Simplescalar
The repository contains the link to source codes required for running the simulator and instructions how to install and run it.

Installation Instructions:

1) Download the source code of simplesim3 from http://www.simplescalar.com/agreement.php3?simplesim-3v0e.tgz

2) Make a directory called "simplescalar" in your local machine.

3) Simplescalar is incompatible with current systems. So, to make it work, follow the technique found out by Sebastian which he has posted on Github: https://github.com/sebastian2696/SimpleScalarUbuntu. You can clone this in your local machine.

4) Within the directory "build", you have to place the source code.

5) Now, outside build directory, you have to execute the script: ./installscript_32.sh

6) After running the script, run this: source ~/.bashrc

 All credits to Sebastian to help you traverse this road.
 
 Running the Benchmarks:

Part 1:

1) Download four benchmarks: spec95-little, spec95-big, Benchmarks and BenchMarks_Little folders from the repository of Simplescalar
2) Save them in your local machine first
3) Uncompress spec95-little and spec95-big in the folder where you install simplescarlar
4) Uncompress benchmars and benchmark_little in simplesim-3.0
5) open terminal in simplesim-3.0
6) run (make clean)
7) run (make config-alpha)
8) run (make)
9) run (./sim-profile -h) to print help message. 
10) run cc1 benchmark (./sim-profile -iclass benchmarks/cc1.alpha -O 1stmt.i ) 
11) read the output
12) run anagram benchmark (./sim-profile -iclass benchmarks/anagram.alpha words <benchmarks/anagram.in> OUT)
13) check your result
14) run compress95 benchmark (./sim-profile -iclass benchmarks/compress95.alpha <benchmarks/compress95.in > OUT)
15) check your result
16) run go benchmark (./sim-profile -iclass benchmarks/go.alpha 50 9 2stone9.in >OUT )
17) explore other commands (replace -iclass with other options in help message) 
    For example: run (./sim-profile -all benchmarks/cc1.alpha -O 1stmt.i)
    
    

 
 
