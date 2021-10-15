This document will decribe the detail steps for usage of GALAXY code. I hope it can be carry out step by step that is user friendly especially for the beginner at astronomy without any preparatory knowledge about simulation and shell programming, treat the whole process works like a blackbox without any concern on the code structure and simulation details. 

# Sec 1. The principle process.

1. Paramter File Setiing: edit a ASCII file that must be named as runX.dat$, where 11<=X<=1000  should be an integer as the run number of the simulation.

2. Particle File Creating: write a script running mkpcs, don't be worried about it if you know nothing about script and shell programming and just follow the detailed steps as below, to set up a .pcs file as the initial conditions or the particles' file for the simulation.

3. Evolution File Creating: use the pcs2dmp to read the .pcs file creat in Step2, this will output a .dmp file as the evolution file to run the simulation. (It can view this .dmp file as the mock galaxy at different time slices, or similar to the discrete nodes for numerical integration.) 

4. Run Simulation: use the galaxy to integrate the evolution.

RK: don't worried about anything that you unclear with in this part, this section is only a brief overview of the process.

# Sec 2. Editting the runX.dat$ File

1. Download the template runX.dat file on my GitHub. (There is also a more a brief file run11.dat$ provided for process test.)

2. Modify the file as you want, the words after the pound sign is only explation for understaning the parameters meaning. 

A complete decription about the partemeters is available in Sec5 in the online manual of GALAXY(http://www.physics.rutgers.edu/~sellwood/manual.pdf). This template is a trial repeat of the ModelA in Sellwood & Gerhard 2020(https://ui.adsabs.harvard.edu/abs/2020MNRAS.495.3175S/abstract).

3. RK: not all the parameters required, and some optional parameters are necessary for some cases, check it patiently. Later May be a summary on each case.

# Sec 3. Create the .pcs File

Only for Test at Now!!! Modify Later.

1. Download the run11s.sh file on my GitHub.

2. Copy such file to your working directory (the same one as the .dat file).

3. modify the absolute path of the executable programe smooth & mkpcs in this file (line3 & line22)

4. -$ chmod +x run11s.sh

5. -$ ./run11s.sh

RK: after the above steps, a .pcs file will be created at the working directory.

!!!Required checking!

# Sec4. Run galaxy

Similar as Sec5.

1. Download 

2. Exectute

