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

Part 2:

18) Open terminal in simplesim-3.0
19) run (make clean)
20) run (make config-pisa)
21) run (make)
21) run (./sim-profile -iclass BenchMarks_Little/cc1.ss -O 1smt.i)
23) run (./sim-profile -iclass BenchMarks_Little/anagram.ss words <BenchMarks_Little/anagram.in> OUT)
25) run (./sim-profile -iclass BenchMarks_Little/compress95.ss <BenchMarks_Little/compress95.in> OUT)
27) run (./sim-profile -iclass BenchMarks_Little/go.ss 50 9 2stone9.in > OUT)
28) explore other commands
29) run following command will execute the compress95 benchmark and print the output to compress95.out and log the execution trace to compress95.trace in the Results folder
    (./sim-outorder BenchMarks_Little/Programs/compress95.ss < BenchMarks_Little/Input/compress95.in  2> BenchMarks_Little/Results/compress95.trace > BenchMarks_Little/Results/compress95.out)
30) The below command will execute the go benchmark and print the output to go.out and log the execution trace to go.trace in the Results folder
    ./sim-outorder BenchMarks_Little/Programs/go.ss 50 9 BenchMarks_Little/Input/2stone9.in  2> BenchMarks_Little/Results/go.trace > BenchMarks_Little/Results/go.out
31) Before executing the anagram program place the words file from the Input folder in the simplesim-3.0 directory. The below command will execute the anagram benchmark and print the output to anagram.out and log the execution trace to anagram.trace in the Results folder
    ./sim-outorder BenchMarks_Little/Programs/anagram.ss words < BenchMarks_Little/Input/anagram.in  2> BenchMarks_Little/Results/anagram.trace > BenchMarks_Little/Results/anagram.out
32) The below command will execute the cc1 benchmark and print the output to 1stmt.s in the Programs folder and log the execution trace to cc1.trace in the Results folder
    ./sim-outorder BenchMarks_Little/Programs/cc1.ss -O BenchMarks_Little/Input/1stmt.i 2> BenchMarks_Little/Results/cc1.trace
33) Before executing the perl program place the perl-tests.pl file from the Input folder in the simplesim-3.0 directory. The below command will execute the perl benchmark and print the output to perl.out and log the execution trace to perl.trace in the Results folder
    ./sim-outorder BenchMarks_Little/Programs/perl.ss < perl-tests.pl 2> BenchMarks_Little/Results/perl.trace > BenchMarks_Little/Results/perl.out
34) check your result in Result folder
    
    

 
 
