PowerShell Cmdlet
Basic Cmdlets
Cmdlet	Description	Example Usage
Get-Help	Shows help information about commands	Get-Help Get-Process
Get-Command	Lists all available commands	Get-Command
Get-Content	Displays the content of a file	Get-Content C:\example.txt
Set-Content	Writes or replaces content in a file	Set-Content C:\example.txt "Hi"
Select-String	Searches text/files for specific patterns	Select-String -Pattern "error" log.txt
Where-Object	Filters objects based on a condition	`Get-Process
Sort-Object	Sorts objects by property	`Get-Process
Out-File	Sends output to a file	`Get-Process
Get-Variable	Gets variables in the current session	Get-Variable
Set-Variable	Creates or changes variables	Set-Variable -Name MyVar -Value 1
Clear-Host	Clears the screen	Clear-Host
Measure-Object	Measures properties of objects	`Get-ChildItem
Write-Output	Sends output to the pipeline or console	Write-Output "Hello, world!"
Write-Host	Displays colored output on console	Write-Host "Success" -ForegroundColor Green
Get-History	Shows command history	Get-History
Invoke-History	Runs a command from history	Invoke-History 3
Get-Alias	Gets command aliases	Get-Alias
Set-Alias	Creates an alias for commands	Set-Alias ll Get-ChildItem
ForEach-Object	Performs an operation on each item in a collection	`Get-Process
Get-Location	Shows the current directory	Get-Location

File System Cmdlets
Cmdlet	Description	Example Usage
New-Item	Creates new files or directories	New-Item -Path "C:\Test" -ItemType Directory
Copy-Item	Copies files or folders	Copy-Item C:\file.txt D:\Backup\file.txt
Move-Item	Moves files or folders	Move-Item C:\file.txt D:\Archive\file.txt
Remove-Item	Deletes files or folders	Remove-Item C:\Temp\* -Recurse
Rename-Item	Renames a file or folder	Rename-Item "old.txt" "new.txt"
Get-ChildItem	Lists files and folders in a directory	Get-ChildItem C:\Temp
Test-Path	Checks if a path exists	Test-Path C:\Temp
Get-Item	Gets a specific file or folder	Get-Item C:\file.txt
Set-Item	Changes the value or content of an item	Set-Item -Path Env:Path -Value $newPath
Join-Path	Combines strings into a path	Join-Path C:\Temp "file.txt"
Split-Path	Gets part of a path	Split-Path C:\Temp\file.txt -Parent
Clear-Content	Clears the content of a file	Clear-Content C:\log.txt
Get-ItemProperty	Gets properties of a file or folder	Get-ItemProperty C:\file.txt
Set-ItemProperty	Sets properties of a file or folder	Set-ItemProperty C:\file.txt -Name IsReadOnly -Value $true
Copy-ItemProperty	Copies properties from one item to another	Copy-ItemProperty C:\file1.txt C:\file2.txt
Get-PSDrive	Lists drives available (file system, registry)	Get-PSDrive
New-PSDrive	Creates a new drive	New-PSDrive -Name X -PSProvider FileSystem -Root C:\
Remove-ItemProperty	Deletes property of an item	Remove-ItemProperty -Path C:\file.txt -Name IsReadOnly
Get-ChildItem -Recurse	Lists all items in directory and subdirectories	Get-ChildItem -Recurse C:\Temp
Format-Table	Formats output as a table	`Get-ChildItem

Network Cmdlets
Cmdlet	Description	Example Usage
Test-Connection	Checks network connectivity (like ping)	Test-Connection google.com
Get-NetIPAddress	Shows IP address information	Get-NetIPAddress
Get-NetIPConfiguration	Displays IP configuration details	Get-NetIPConfiguration
Get-NetAdapter	Gets network adapter information	Get-NetAdapter
Enable-NetAdapter	Enables a network adapter	Enable-NetAdapter -Name "Ethernet"
Disable-NetAdapter	Disables a network adapter	Disable-NetAdapter -Name "Wi-Fi"
Set-DnsClientServerAddress	Sets DNS servers for a network adapter	Set-DnsClientServerAddress -InterfaceAlias "Ethernet" -ServerAddresses ("8.8.8.8")
Get-DnsClientServerAddress	Gets DNS server addresses for adapters	Get-DnsClientServerAddress
Test-NetConnection	Tests network connection with detailed info	Test-NetConnection google.com -InformationLevel Detailed
Resolve-DnsName	Performs DNS query	Resolve-DnsName google.com
Get-NetRoute	Gets IP route information	Get-NetRoute
New-NetIPAddress	Adds a new IP address to an interface	New-NetIPAddress -InterfaceAlias "Ethernet" -IPAddress 192.168.1.10 -PrefixLength 24
Remove-NetIPAddress	Removes IP address from interface	Remove-NetIPAddress -IPAddress 192.168.1.10
Get-NetFirewallRule	Lists firewall rules	Get-NetFirewallRule
Enable-NetFirewallRule	Enables a firewall rule	Enable-NetFirewallRule -Name "FPS-Rule"
Disable-NetFirewallRule	Disables a firewall rule	Disable-NetFirewallRule -Name "FPS-Rule"
Show-NetConnectionProfile	Displays network connection profile	Get-NetConnectionProfile
Get-NetIPAddress -AddressFamily IPv6	Shows IPv6 addresses	Get-NetIPAddress -AddressFamily IPv6
Restart-NetAdapter	Restarts a network adapter	Restart-NetAdapter -Name "Wi-Fi"
Get-NetNeighbor	Displays neighbor cache entries	Get-NetNeighbor
