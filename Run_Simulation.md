This is the description about how to run a simulation on Gravity server.

# Sec1. Editting The .dat File

GALAXY simulation code using a ASCII file named as runX.dat file to organize the parameters required by the target model.

RK: X is the ID number only for distinguish different simulation project. It must be an integer in the range 11~9999.

\\

For searching easiness, using the section classfication method of the parameters the same as the GALAXY online manual.

## User Friendly Steps:

Step1: creating your working directory, cd into it.

Step2: cp the corresponded grid method's .dat file in GALAXY15/EXAMPLES/c3d (as an example).

Step3(opitional): modify the the parameters as you need.


## Complete Steps:

PartA: The ID number and grid method (which method using for gravity calculation) part.

Step1: run no			X  (The X only for distinguishin)

Step2: grid type		c3d (or other method you want) (different method may need different parameters in below)



Part B
## Decription on the parameters meanning

# Sec2. Editting the shell script for interactive simulation running.

Almost all the GALAXY subroutines works in a user interactive way. Using a shell script to origanize the whole process is recommended.

As in the EXAMPLES of the GALAXY15, I devide the whole process into two distinct part: initial condition creating script (in the EXAMPLE subdirectory of GALAXY15, it is usually named as  runXs.s), and the simulation run script (runX.s in EXAMPLES). 

## User Friendly Steps:
Step1: in the same working directory as in Sec1, cp the runXs.s file in the EXAMPLE/c3d (as an example) to the working directory. (RK: the X should be the same as the previous runX.dat file)

Step2: modify the programme path in the runXs.s file. vim it, edit your path similar as "mypath=/home/<your user name on gravity>/<your directory to the GALAXY15/bin file>", then add "$mypath" to the beginning at such lines which begin with some executable program that with the word ">> eof". Save and exit.

OR: Step2 (easier by not recommended): simply copy all the programs in GALAXY15/bin/ to your working directory.

Step3: repeat Step1 & Step2 to the runX.s file, again the X should be same.
## Complete Steps:


# Sec.3 Using the queues script .qsub file to submmit your job on the calculation node.

Step1: touch a .qsub script on your working directory

Step2: copy the example script on https://gravity-doc.github.io/Basic/Job.html Sec.Basic.3 to your .qsub file

Step3: modify the command below the line "# run your own program!!!", recommend:

cd /home/<your user name on gravity>/<your working directory>/

chmod +X runXs.s

chmod +X runX.s

./runXs.s

./runX.s

\\

Done it!
