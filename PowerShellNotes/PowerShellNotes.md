# Powershell Notes

### What is an opertating system?

An operating system is the system software that mangages computer hardware and software resources and provides common services for computer programs.

##### What does OS consist of?

* Bootloader
* Kernel
* Daemons
* Networking
* Shell
* GUI
* Application

##### Kernel

* Kernel is the core of computer's OS and controls ALL tasks of a computer.
* It cannot be overwritten

![Computer Architecture](https://cdn.discordapp.com/attachments/955109188609114135/1079352078855569428/image.png)

##### Shell Commands

* powershell: use powershell
* ping 8.8.8.8: send a series of packet to the google's public dns server(8.8.8.8)
* cd or cd "path": change directory
* cd ~: home folder
* mkdir: create directory
* ls: get all files in the directory
* ls -R: get recursive directory, means getting subdirectories
* echo "text-file": displays file name
* echo "message" > text-file: add message to text file (or replace if text already exists)
* echo "message" >> text-file: add extra message to text file (\n for a new line)
* cat text.txt: display content in the text.txt
* copy text.txt "path\text2.txt": copy file to the destination and rename it as text2.txt
* copy text.txt text2.txt: copy file and rename it as text2.txt
* Copy-Item -Path "path" -destination "path": copy an item from one location to another
* remove file or rm file: delete specific file
* del -R folder: delete the specific folder

### PowerShell ISE

##### Difference between Powershell ISE and Powershell

PowerShell is a command line interface, PowerShell ISE offers a graphical user interface and is more beginner-friendly.
PowerShell is for directly executing commands while PowerShell ISE is more about testing and debugging scripts.

##### other commands
get-command: get all commands 
get-command * > Powershell-commands.txt: save all commands into Powershell-commands.txt
get-process: get all processes
get-process | select name,cpu |sort cpu| out-gridview: saves name and cpu columns in a gridview that is sorted by cpu
echo "" > PowerShellScript.ps1: create an empty script/batch file named PowerShellScript

##### What is a ps1 file?

A script is a plain text file that contains one or more PowerShell commands, 
and PowerShell scripts have a .ps1 file extension.