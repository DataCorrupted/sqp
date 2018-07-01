# Sequential Quadratic Optimization

An inexact penalty quadratic optimization for large-scale problems.

## Folders & Usage

### sif

This folder includes all the problems we tested. For detailed problems see the README in this folder.

Please copy all the sif file into this folder and run:

	./decode.py

It will call _sifdecoder_ and turn all your .sif file into a folder with decoded problems.

### cutest_py

A python-cutest interface written by Jianshan Wang. Some files are missing, please make sure that you have cutest installed and then run:

	./collect_files.sh

to collect all the files needed to compile the interface.

To compile run:

	./make_all ../sif

Currently it will only compile on 64bit linux machine. I will try to make it more generic in the future. 

It will compile the interface along with the .f file in each and every problem in the sif folder. It will dump the dynamic linked library in each problems folder generated in last step.

### src

All the codes should be here. Run:

	python run_experiment.py

to start an experiment.

Use

	python output_summary.py

you can generate a latex file containing a table of all the results of the problems you just tested.