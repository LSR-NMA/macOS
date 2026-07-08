## Windows

- [x] Install software downloaders (Windows Store, chocolatey, winget)
- [x] Install python install manager on Windows Store
- [ ] Install Microsoft Office
- [ ] Install Powertoys

**Powershell script to re-set up Windows after every reset**

```
# Installs Windows Store
wsreset -i 

# Install chocolatey
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

choco install winget -y

irm https://get.activated.win | iex




```
