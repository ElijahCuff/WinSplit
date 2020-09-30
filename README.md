# WinSplit
The WinSplit Project was designed to make Self Extracting Archives with your preferred File Binding solution.


This project was designed to build WinRAR SFX Archives  in EXE format for windows PC's - Using various different platforms and code languages.
 
 
The initial idea came after learning about 7zip's SFX Stub File,
 
The 7z Stub File can be prepended to a Zip file to create a self extracting archive, however this method lacks many desired options like "Silent Extraction" - "Automatic Overwrite" - "Icon File Support at compile time" - "Licence Screens" and various other features of other SFX Archives.
 
After many hours i found that WinRAR also uses an SFX Module, not a Stub but a Module.
 
The Module allows all the features that 7zip's Stub file doesn't support.
 

This brought about 2 problems,
The SFX Archive is only able to be Built in the WinRAR software because they don't release the WinRAR SFX Stub files for people to work with.
 
The SFX Module is not able to be prepended to a Zip file like the 7zip Stub, instead it is a compilation of Multiple Stubs placed at different locations in the final build.
 
    
Eventually i got a distributable archive built using the windows version of WinRAR and started comparing Hex representatives of the binary in files with / without icons, Changing Zip files and comparing etc...     
    
This lead me to extract 2 of the 3 stub files that need to be merged in succession,     
   
1- Start Stub - Main SFX file, Prior to .Ico file   
2- Prepared .Ico File   
3- Second Stub - Another Program that is the UI   
4- Zip Appended with Commamd Comments   
      

The prepared .ICO file required removing everything before the Key, it took a while to find the Hex Key for all .Ico files, but i finally got the hex search query "key" that defines the Start of the prepared .ico to the end of the file. - I've written the key into a text file in this folder.
   

You need to find the .ico key and then Cut everything after that into the prepared.ico file ready for merging.
   
The Final Seperation of the archive i couldn't be bothered doing because i was only interested in Silent Installs, - Thats the User Interface Image - An image appears under your logo when Extracting - This image i couldn't be bothered splitting out because it is not visible under a Silent Install.
   
    
## Building a Test EXE,    
Merge Files In Succession, using whatever file binding method you prefer.
