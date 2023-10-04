# Enabling WinRM
Enable-PsRemoting -Force

# Make sure the WinRM service is setup to start automatically
Set-Service WinRM -StartMode Automatic

# Verify start mode and state - it should be running
Get-WmiObject -Class win32_service | Where-Object {$_.name -like "WinRM"}

# Trust all the hosts in WinRM. Note, in a Production environment, you do not want to do this.
Set-Item WSMan:localhost\client\trustedhosts -Value *

# Checking that all the hosts are trusted
Get-Item WSMan:\localhost\Client\TrustedHosts

# Opening the WinRM HTTP port in the Firewall (for HTTPS use port 5986)
netsh advfirewall firewall add rule name="WinRM-HTTP" dir=in localport=5985 protocol=TCP action=allow