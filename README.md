# environment-variable-dll-hijacking
Project base on the work of @Wietze on twitter utilizing process level environment variables to have a malicious DLL loaded by a trusted process.

Source-Files contains either templates for compiling DLLs for hijacking use or a dummy.cpp file that is not yet working to be loaded by processes.

dll-attempts contains a .def file that creates the exports of the targeted dll that will need to be used in your malicious dll you are trying to have loaded as well as two compiled dlls that have been able to be loaded by changing a process level environment variable.

Get-Hijackable tests almost all executable in the c:\windows\system32 directory to see if they are vulnerable to this kind of DLL hijacking.

Change-Environment changes the SYSTEMROOT environment variable for one specific process to point to your own c:\"something"\system32\ directory.
