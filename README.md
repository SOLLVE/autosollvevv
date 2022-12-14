
# autoSOLLVEvv

autoSOLLVEvv is an automation command line tool for SOLLVE V&V


This project aims to bridge the gap between the SOLLVE V&V testsuite and the Application Developers/Vendors/Facilities by making the testsuite more accessible by building an interactive and easy to use command line interface tool. This CLI tool seeks to inform its users of the compiler/runtime failures that have already been declared as bugs by the testsuite.

The current version of this tool is built for use on the pre-exascale system Crusher


## Installation

The installation media is located in the UMS012 space on Crusher at /sw/crusher/ums/ums012/SOLLVE/autosollvevv/


The installation requires Python3 and pip3 dependencies.
```bash
pip3 install -e /sw/crusher/ums/ums012/SOLLVE/autosollvevv/
```
The -e installation option is for --editable, by which the user wouldn't have to install newer versions as the current version will automatically be updated without the need for reinstallation.

```bash
mv .local/bin/autosollvevv .
```
This command is used to move it from the installation directory to the user's working directory. This needs to be done as the user's doesn't have the privileges to make autosollvevv an environment variable using pip3.



## Usage

```bash
python3 autosollvevv file
```


```bash
positional arguments:
  file                  This is to input the program file

optional arguments:
  -h, --help            show this help message and exit
  -c {llvm,rocm,cce}, --compiler {llvm,rocm,cce}
                        This is to specify the compiler to show all versions
  -cv {llvm_14,llvm_15,llvm_16,rocm_4.5,rocm_5.0,rocm_5.2,cce_14.0.0,cce_14.0.1}, --compilerversion {llvm_14,llvm_15,llvm_16,rocm_4.5,rocm_5.0,rocm_5.2,cce_14.0.0,cce_14.0.1}
                        This is to specify the compiler with its version
  -omp {4.5,5.0,5.1,5.2}, --openmp {4.5,5.0,5.1,5.2}
                        This is to specify the OpenMP Version

```
