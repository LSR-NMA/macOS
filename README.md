First, set up automation scripts for setting up Windows after a factory reset.
Second, install macOS on Lenovo T480 to dual-boot between Windows and macOS to be able to use specific statistics applications, etc. and create desktop application versions for both platforms.

## Windows

- [x] Install software downloaders (Windows Store, chocolatey, winget)
- [x] Install python install manager on Windows Store
  - [ ] Install jupyter notebook, etc.
- [x] Install Microsoft Office
- [x] Install Powertoys

**Powershell script to re-set up Windows after every reset**

```
# Installs Windows Store
wsreset -i 

# Install chocolatey
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))

choco install winget -y

irm https://get.activated.win | iex




```
