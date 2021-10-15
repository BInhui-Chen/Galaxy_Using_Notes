This is the process of 

(1) download and compile the GALAXY code on the Gravity

(2) the process to run a simulation (Take Sellwood & Gerhad 2020 Model A as examples)

# 1.Download Section

1. Just go to the website http://www.physics.rutgers.edu/galaxy/

2. Enter your email (for notification of the version update only)

3. Click the download, waiting for a moment, the compressed file, galaxy.tar or .tzp, of the bundle files construct the GALAXY will download to your computer.

RK: the download file is tiny, only a few Mbs. 

# 2.Compile Section

!!! Require modification!

1. Decompressed the galaxy.tar(tgz): change to the directory of the galaxy.tar file (on Gravity using terminal, the Jupyter Lab doesn't work!)

2. -$ tar xvf galaxy.tar OR tar xzf galaxy.tgz (opitional: rm the .tar file), then there will be a GALAXY15 folder in the same directory

3. -$ module load mpi/openmpi-3.1.1 (load the mpi module for the mpi usage of GALAXY)

4. -$ cd GALAXY15/SRC/lib15

5. -$ ./rebuild

6. -$ cd ../RAJ

7. -$ ./rebuild

8. -$ cd ../utils

9. -$ ./rebuild

10. -$ cd ../lib15_mpi

11. -$ ./rebuild

12. -$ cd ../progs

13. edit the PATH of the PGPLOT object library in the Makefile (in the progs directory): change the line begin with "pgplot_lib = "(line 9), replace the later words in the line by the correct PATH

14. edit the same Makefile line that begins with "sys_lib = ", replate later words in the line by -lgfortran -L/usr/X11R6/lib64 -L/usr/lib64 -lX11 -lpng

15. -$ make

16. -$ make clean

17. -$ cd ../progs_mpi, repeat the same operations as step.14 to step 16. RK: Do not repeat step 13!

You have done it!😁😁😁
