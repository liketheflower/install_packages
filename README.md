# install_packages


# install Mayavi









# install VTK

http://sese.nu/517-2/


on linux:
Via the package manager (recommended)

VTK can be found in the package repository on most Linux distributions, making the installation process quick and painless. For instance, on Ubuntu 12.04 you can install VTK 5.8 and the Python wrapper by typing

sudo apt-get install libvtk5-dev python-vtk


on mac

http://www.cb.uu.se/~johan/vtk/installing_vtk_on_mac.txt




# ERROR 1: ImportError: No module named vtk



# ERROR 2:  > import vtk
Traceback (most recent call last):
  File "/Users/jimmy/Dropbox/VTK/VTK-7.1.1/Wrapping/Python/vtk/vtkCommonCore.py", line 5, in <module>
  
  
    from .vtkCommonCorePython import *
ImportError: No module named 'vtk.vtkCommonCorePython'


Solution:  

$ /home/vtk/bin/vtkpython
vtk version 6.2.0
Python 2.7.5 (default, Mar  9 2014, 22:15:05) 
Type "help", "copyright", "credits" or "license" for more information.
>>> import vtkCommonCorePython 
>>> print vtkCommonCorePython
<module 'vtkCommonCorePython' from '/home/vtk/lib/vtkCommonCorePython.so'>


# error 3:  

>>> import vtk
Fatal Python error: PyThreadState_Get: no current thread
Abort trap: 6


solution:
remove the "/Users/jimmy/Dropbox/VTK/VTK-7.1.1/lib" from the environment varialbe PYTHONPATH
then the problem is fixed, however, the error 2 will appear instead.
