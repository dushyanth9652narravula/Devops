# Tools Setup for Devops

- To Learn devops, we need to configure our software by installing some tools and signup for some accounts. Mainly we need to do the following 3 steps to learn devops.

  1) **Installation of Tools**
  2) **Signup Accounts**
  3) **Aws Setup**

## Installation of Tools

- To learn devops we need to install the following tools :

  1) **Oracle Vitual box**
  2) **JDK**
  3) **Git**
  4) **Maven**
  5) **Vscode**
  6) **Vagrant**
  7) **Sublime Text Editor**
  

- So, inorder to install all these tools we need to thier offical website and ten download the installers and then we need to install manually in our system.

- Instead of their official websites individually, we can install of these tools by using one software which is <b>Chocolatey</b>

- <b>Chocolatey</b> is a software which is used to install other software by using command line or powershell

- To install Chocolatey on windows system just follow these steps :

  1) First open the powershell in Administrator Mode.

  2) Then Run this command `Get-ExecutionPolicy`. If it returns <b>Restricted</b> then run tis command `Set-ExecutionPolicy AllSigned` which returns <b>AllSigned</b>

  3) After you get <b>AllSigned</b> then run the following command which automatically installs chocolatey.

     `Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))`

  4) If you need any further assistance chaeck the following website [Chocolately](https://chocolatey.org/install)

  5) After installing the Chocolatey, just run `Choco list` which gives whether choclately is installed or not.

  6) After installing choclatey, then you need just need to run te following command in powershell to install all te required tools.

     **Virtual Box** : `choco install virtualbox --version=7.1.4 -y`

     **Vagrant** : `choco install vagrant --version=2.4.3 -y`

     **Git** : `choco install git -y`

     **Maven** : `choco install maven -y`

     **Correto7jdk** : `choco install corretto17jdk -y`

     **AWSCLI** : `choco install awscli -y`

     **VsCode** : `choco install vscode -y`

     **Sublime Text Editor** : `choco install sublimetext3 -y`

     **Note** : If you want to install any other software using chocolatey then search for that software in this website which gives `choco` command to install that software [Other Software Installation](https://community.chocolatey.org/packages). You may get advanced versions of these softwares at that the of your installation. So please install that advanced versions by using the above link.

## Signup Accounts

- In order to learn devops we must need to signup these accounts.

  1) [GitHub](https://github.com/)

  2) [DockerHub](https://hub.docker.com/)

  3) [SonarCloud](https://sonarcloud.io)

- Just create account in all these 3 websites. Create account in SonarCloud using github account.

