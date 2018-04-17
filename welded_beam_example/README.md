# THE WELDED BEAM DESIGN PROBLEM

The Jupyter notebook presents the optimization of a real-world problem (Welded Beam Design) with a multiobjective optimization algorithm (NSGA-II).

# Getting Started
These instructions will get you a copy of the notebook up and running on your local machine for testing purposes. 

# Prerequisites
Conda, for example, Miniconda: https://conda.io/miniconda.html

Documentation: http://conda.pydata.org/docs

# Installing
1. Download source files from git: 
```
git clone https://github.com/synergy-twinning/summer-school/
```
2. Go to folder of source files: 
```
cd ./summer-school/welded_beam_example
```
3. Create Conda environment:
```   
conda env create -n synergy-summer-school -f environment.yml
```
4. Activate environment (to be done each time you open a new terminal window):

Windows:
```
activate synergy-summer-school
```
Linux:
```
source activate synergy-summer-school 
```

# Compiling external library
If the precompiled libraries (EvaluationFunctions.so or EvaluationFunctions.dll) are not compatible with the local system, they should be recompiled.
To this end, execute:

Windows:
```
g++ -c EvaluationFunctions.cpp
g++ -shared -o EvaluationFunctions.dll EvaluationFunctions.o -Wl,--out-implib,libexample_dll.a
```
Linux:   
```
g++ -fPIC -shared EvaluationFunctions.cpp -o EvaluationFunctions.so
```
   
# Running
Execute command:
```
jupyter notebook --notebook-dir=.
```
   
# Uninstalling
1. Remove folder with source files
2. Uninstall Conda environment:
```
conda env remove -n synergy-summer-school
```
3. Remove Conda

# Running on cloud without installing
To run without installing, go to: https://mybinder.org/v2/gh/synergy-project/summer-school/master?filepath=SynergySummerSchool.ipynb

Note that this is a publicly available service whose resources are limited. Consequently, it becomes unavailable when requests exceed the available resources.
Therefore, the link should be accessed a few times until the resources become available and the environment is set up.

