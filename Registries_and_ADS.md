reg query HKU\S-1-5-21-2881336348-3190591231-4063445930-1003\Software\Microsoft\Windows\CurrentVersion\Run
#retreives suspcious value hidden within this registry key.

reg query HKLM\Software\Microsoft\Windows\CurrentVersion\RunOnce
#retreives suspcious value hidden within this registry key.

reg query HKU\S-1-5-21-2881336348-3190591231-4063445930-1003\Software\Microsoft\Windows\CurrentVersion\RunOnce
#retreives suspcious value hidden within this registry key.

reg query HKLM\Software\Microsoft\Windows\CurrentVersion\Run
#retreives suspcious value hidden within this registry key.

reg query "HKEY_LOCAL_MACHINE\Software\Microsoft\Windows NT\CurrentVersion\N
etworkList\Profiles\{20A9DB9D-5643-46F7-9FC7-0C382A286301}"
#Retrieves suspicious value hidden within this registry key (the suspiscious network).

reg query "HKLM\System\CurrentControlSet\Enum\USBSTOR"
#Retreives suspicious value hidden within this registry key (the suspicious USB).

gci registry::HKU
#this command will allow you to see the contents of the provided registry, including HKU, without the issue of errors if you didn't include the 'registry' option. 


Get-localuser -name $env:USERNAME | select-object sid
Get-localuser -name $env:'Student' | select-object sid
Get-ChildItem -Path "HKLM:\Software\Microsoft\Windows NT\CurrentVersion\ProfileList
#Ways to locate profiles (suspicious as well) within the registry, to incude their SIDS. 

C:\ProgramData\Microsoft\Windows\WlanReport\wlan-report-latest.html
$LET THE INSTRUCTORS KNOW THAT YOU ADDED THIS ON ACCIDENT

get-childitem -force 
#will list all files in the current directory, regardless of attributes.

get-filehash -algorithm SHA512
#Gives the sha512 hash of a file in windows powershell. 

get-acl
#powershell command that lists the permissions of a file

C:\Windows\System32\drivers\etc\hosts
#the file that maps hostnames to IP addresses in Windows

icacls "C:\Windows\System32\drivers\etc\hosts"
#lists the permissions of the specified file, (path provided to the file hosts). RX is read and execute, which is permitted by the group: Builtin\Users.

certutil -hashfile "C:\Windows\System32\drivers\etc\hosts" MD5
#provides the md5 hash of the provided file, which is an MD5 hash in this case, for the file 'hosts'.

dir /s /b "readme"
#syntax to search for a specific file (or string) within the present and sub directories of the current directory. 

dir /a 
#shows all--to include hidden--files within the current working directory. 

dir z*
#if a file path is too long to copy and paste, try using the dir command with a wildcard to capture the remainder of the filepath that cannot be pasted. 

dir /a /s /R | findstr "DATA"
#You can locate hidden ADS's using this. /a is all, /s is subdirectories, and the /R is specfically for files with an ADS. Findstr is the same as grep, and matches a string that has 'DATA' in it, which is commonly next to the ADS. 


openssl enc -d aes-128-key -a -salt -in /home/garviel/Encrypted








Get-Process | where-object {$_.SI -eq '0'}
#Will display session process that starts at the system 0 level.









