# num7 STATIC AND DYNAMIC LIBRARIES FOR WINDOWS 10/11

    g++ -std=c++14 -shared num7.cpp -o num7.dll #num7.dll BUILDING UP DYNAMIC LIBRARY  
    
    g++ -std=c++14 -c num7.cpp -o num7.lib      #num7.lib BUILDING UP STATIC  LIBRARY 
    
    Place the DLL in the same directory as the executable:  
        The easiest way is to place the .dll file in the same folder as the executable (.exe) that is using the DLL.  
        Windows will automatically look for the current directory (where the .exe is located) when attempting to load a DLL.  
    
    g++ -std=c++14 test_num7_eligibility.cpp num7.lib 	   #a.exe STATIC  LIBRARY  
    
    g++ -std=c++14 test_num7_eligibility.cpp num7.dll -o b.exe #b.exe DYNAMIC LIBRARY
