# XcodeMexProjectTemplate
A Project template for creating Matlab mex files

Much of this came from the  files at  http://au.mathworks.com/matlabcentral/answers/125043-how-to-build-and-debug-matlab-mex-file-with-xcode-5-1-ide-on-os-x which don't work with Xcode 6 (they cause Xcode to crash) my work simplifies the process and the location for install specified at the above link is not correct and will be overwritten at every update of XCode better to install as shown below.  
I have also added the files for a hello world application.


1) mkdir -p $HOME/Library/Developer/Xcode/

2) Then put the folder Templates from the git respository into $HOME/Library/Developer/Xcode/
3) Open Xcode 6 and select 'File -> New -> Project' In the left column choose Templates and then select MEX.
4) The 'Product Name' should be the same as the name of the MEX-function you wish to create.
5) Enter the name of the MATLAB application as it appears in finder the default is 'MATLAB_2015a'. This is used to create paths to the library and header files contained within the Matlab application bundle.
6) Choose a location for you mex project.
7) You now have a project with a function that prints hello world. You can build it by selecting 'Product-> Build For-> Testing.

NOTE if this fails it is probably because the configuration in the generated .xcconfig has not been selected you can do this by using the 'Project Navigator' to look at the 'info' page for the project then by selecting the only configuration available for both debug and release builds.  I hope to work out how to make the template set these two values automatically soon.

8) You debug by attaching to a running instance of Matlab by selecting 'Debug->Attach to Process->Matlab' 
9) Set a breakpoint in the Hello World source code somewhere (by clicking on the line number at the line you want to set the breakpoint at), set Matlabs path to point to the folder where the newly built mex file is and then type the name of the mex function in Matlab. The debugger should come up when you hit the breakpoint set in the source code.



