reg query HKU\S-1-5-21-2881336348-3190591231-4063445930-1003\Software\Microsoft\Windows\CurrentVersion\Run
#retreives suspcious value hidden within this registry key.

reg query HKLM\Software\Microsoft\Windows\CurrentVersion\RunOnce
#retreives suspcious value hidden within this registry key.

reg query HKU\S-1-5-21-2881336348-3190591231-4063445930-1003\Software\Microsoft\Windows\CurrentVersion\RunOnce
#retreives suspcious value hidden within this registry key.

reg query HKLM\Software\Microsoft\Windows\CurrentVersion\Run
#retreives suspcious value hidden within this registry key.


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
$provides the md5 hash of the provided file, which is an MD5 hash in this case, for the file 'hosts'.



