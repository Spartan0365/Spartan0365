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
