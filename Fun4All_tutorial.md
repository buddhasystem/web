# Fun4All Tutorial  
(Library points to Root version 5.34/36)
## First tutorial:
Source the configuration file for PHENIX  
```
      source /opt/phenix/core/bin/phenix_setup.csh -n  
```
Clone the source code  
```
      git clone https://github.com/EIC-Detector/g4exampledetector  
```
Build the source code  
```
      cd g4exampledetector/simple/source/  
      mkdir ../../myinstall  
      mkdir build  
      cd build/  
      ../autogen.sh --prefix=$HOME/fun4all_phenix/g4exampledetector/myinstall  
       make install   
       ERROR   
```       
Asd  

## Second Tutorial:  
Source the configuration file   
```
      source /opt/phenix/core/bin/phenix_setup.csh -n  
```      
Clone the source code  
```
      git clone https://github.com/sPHENIX-Collaboration/tutorials  
```      
Change the directory  
```
      cd tutorials/Momentum/  
```      
Go to the root  
```
      root.exe  
      root [0] .x Fun4All_G4_Momentum.C(-1)  
      ERROR  
```      
Asd

## Third Tutorial:  
Source the configuration file  
```
      source /opt/phenix/core/bin/phenix_setup.csh -n  
```      
Clone the source code  
```
      git clone https://github.com/sPHENIX-Collaboration/tutorials  
```      
Change the directory  
```
      cd tutorials/MyOwnTTree/   
```      
Build the source code   
```
      mkdir build  
      mkdir myinstall  
      cd build  
      ../src/autogen.sh --prefix=$HOME/fun4all_phenix/tutorials/MyOwnTTree/myinstall  
```
Change the code  
```
      vim ../src/MakeSimpleTree.cc  
      vim ../src/AnalyzeSimpleTree.cc  
      Change #include <phool/getClass.h>  
      To  
      #include <getClass.h> 
```      
Build  
```
      make install  
```      
Change the library path
```
      setenv LD_LIBRARY_PATH $HOME/fun4all_phenix/tutorials/MyOwnTTree/myinstall/lib:$LD_LIBRARY_PATH  
```      
Change the directory  
```
      cd ../macro  
```      
Go to root  
```
      root.exe  
      root [0] .x MakeTree.C  
      root [1] .x AnalyzeTree.C  
      root [2] .q  
      root.exe  
      root [0] .x RunBoth.C  
```
Can check the details of all those root files  
```
      root -l mytree.root  
      root [1] .ls  
      root [2] new TBrowser  
```
Finish  
