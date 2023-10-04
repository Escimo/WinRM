## WinRM
After installing the script don't forget to Open the port 5985 in the NSG (inbound)
![nsg-winrm](https://github.com/Escimo/WinRM/assets/1576301/52b6c400-faf3-476b-8deb-82593ccea085)

Again, in a production environment, you will need to secure this.
Add a DNS label to your Public IP DNS (if you’re not using you’re own DNS)
Test that the connection works

### In a *nix/osx environment, use the following command
```
nc -z -w1 <IP or host name> 5985;echo $?
```


PowerShell script for enabling WinRM
