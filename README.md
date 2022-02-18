# windows_dev_environment

Assuming a clean install of Windows, one can proceed with the following steps to configure their workstation for local development of linux based processes.

## Installing WSL and Ubuntu Linux
For more info: https://docs.microsoft.com/en-us/windows/wsl/install
- In Powershell (As Administrator) execute:
    >wsl --install
- Reboot your workstation
- After reboot install "Ubuntu" from the Microsoft Store
- Launch "Ubuntu" from the Windows Start menu
- Allow it to perform first time run steps
- Input desired username and password
- Once configuration is complete, exit "Ubuntu" and restart it
- Now update Ubuntu's apt packages:
    >sudo apt update && upgrade


## Installing Docker in Ubuntu
For more info: https://www.digitalocean.com/community/tutorials/how-to-install-and-use-docker-on-ubuntu-20-04

- In Ubuntu install requirements:
    >sudo apt install apt-transport-https ca-certificates curl software-properties-common
- Add GPG key for official Docker repo:
    >curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
- Add Docker repo to APT sources:
    >sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
- Force apt to use Docker repo:
    >apt-cache policy docker-ce
- Finally install docker:
    >sudo apt install docker-ce

## Cloning a Git repository and editing in VS Code
- In Ubuntu navigate to folder you wish to clone into and execute:
    >git clone [GIT URL HERE]
- Change directories to the cloned repo
- Open the directory in VS Code:
    >code .

