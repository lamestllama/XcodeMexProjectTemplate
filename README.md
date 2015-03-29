# XcodeMexProjectTemplate
A Project template for creating Matlab mex files

Much of this came from the  files at  http://au.mathworks.com/matlabcentral/answers/125043-how-to-build-and-debug-matlab-mex-file-with-xcode-5-1-ide-on-os-x which don't work with Xcode 6 (they cause Xcode to crash) but the instructions are valid. I also added the files for a hello world application.

Also the location for install specified at the above link is not correct and will be overwritten at every update of XCode better to install as shown below.

mkdir -p $HOME/Library/Developer/Xcode/

Then put the folder Templates into /Library/Developer/Xcode/

Now when you open Xcode 6 on Yosemite you get a new Project template.

Give it the name of your install of Matlab the default is MATLAB_2015a it will use this to build a path to the Matlab headers and the Matlab libraries.

You have a Hello World application simply build for debug then attach to a running instance of Matlab.

