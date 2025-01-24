## HOW TO USE:
1. Download [Salome](https://www.salome-platform.org/downloads/previous-versions/salome-v9.4) (Version 9.4 is the best, other versions have not been tested yet)
2. Download [Pfsalome](https://github.com/leoxiaoyuan/PFsalome) and unzip the package to the root of salome modules (e.g. Salome-9.4/SALOME-9.4.0-UB18.04-SRC/BINARIES-UB18.04)
3. Modify the startup script (either salome or mesa_salome). Here, we use salome as an example.
```console
    $ vim salome
```
find '#PRODUCT environment' label and insert <font color=red>'ASTERSTUDY'</font>  after <font color=red>'SMESH'</font>  in the line which setting variables for SALOME_MODULES. Also, we should configurate environment for Pfsalome by add the following lines after the label of <font color=red>'#[all products]'</font> (note:these lines should be added before the code of starting salome and parsing command line arguments)
#[ASTERSTUDY]
context.setVariable(r"ASTERSTUDY_ROOT_DIR", out_dir_Path + r"/BINARIES-UB18.04/ASTERSTUDY", overwrite=True)
```
4. run salome or mesa_salome