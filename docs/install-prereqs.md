# Install Prerequisite Software

The first problem every software development team encounters is how to get developers productive quickly and keep them productive by giving them a consistent development environment that is easy to setup and maintain. Some developers might have Mac laptops while others prefer Windows, and still others prefer Linux; but these environments are very different and do not behave the same.

To solve this problem, will we Visual Studio Code with the Remote Containers Extensions for Docker and be developing in a Debian Linux 11 Docker container. Docker will provide an Infrastructure as Code environment on the developers desktop alone with Visual Studio Code, and a REST tool like Postman. If you don't have this software installed on your development computer, the first step is down download and install them.

**Note:** _The lab will be using a local Debian 11 Linux environment so you will need to know a minimal amount of Unix commands to get around._

## Mac Install using Homebrew

[**Homebrew**]((https://brew.sh)) is my preferred method of installing tools on the Mac. First because it is quick and easy, and second because maintaining the latest version is done for you with a simple `brew upgrade` command. If you are tired of downloading software and keeping it up to date, you want to use `brew` instead:

Install **Homebrew** if you don't have it already:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"
```

Install **Git**, **Docker**, **Visual Studio Code** and **Postman** using the `brew` command

```sh
brew install git
brew install --cask docker
brew install --cask visual-studio-code
brew install postman
```

That will install the necessary software for this workshop onto your Mac. If you don't want to use Homebrew, you can follow the manual installation instructions and install Docker Desktop and VisualStudio Code manually. Postman is optional but recommended.

## Windows using Chocolatey

[**Chocolatey**](https://chocolatey.org/install) is the preferred method of installing tools on Windows. You can install Chocolatey with the following command:

```sh
Set-ExecutionPolicy Bypass -Scope Process -Force; [System.Net.ServicePointManager]::SecurityProtocol = [System.Net.ServicePointManager]::SecurityProtocol -bor 3072; iex ((New-Object System.Net.WebClient).DownloadString('https://community.chocolatey.org/install.ps1'))
```

Install **Git**, **Docker**, **Visual Studio Code** and **Postman** using the `choco` command

```sh
choco install git.install
choco install docker-desktop
choco install vscode
choco install postman
```

That will install the necessary software for this workshop onto your Windows PC. If you don't want to use Chocolatey, you can follow the manual installation instructions and install Docker Desktop and VisualStudio Code manually. Postman is optional but recommended.

## Manual Install

If don't want to use a package manager like Homebrew or Chocolatey, you can manually download and install all of the software needed.

Link to [Git Client](http://git-scm.com/downloads)  

Link to [Docker Desktop](https://www.docker.com/products/docker-desktop)  

Link to [Visual Studio Code](https://code.visualstudio.com/Download)  

Link to [Postman](https://www.postman.com) (optional but recommended)  

Once you have downloaded all of the software please install Docker first and then the rest in any order.

## VSCode Remote Containers

Once you have Visual Studio Code installed, you will need the [Remote Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extensions. You can install it from a shell with this command.

```sh
code --install-extension ms-vscode-remote.remote-containers
```

That will install the Remote Containers extension in your Visual Studio Code. You can also go to the marketplace tab in VSCoe and type "remote" in the search bar and select **Remote Containers** from the list and click **Install**.

## Install the Code Command for Mac

Instructions on how to install the `code` command for Mac can be found here: [Code Command for Mac](https://code.visualstudio.com/docs/setup/mac)

You need to launch VS Code. Then open the Command Palette **(⇧⌘P)** and type 'shell command' to find the Shell Command: _Install 'code' command in PATH command_.

Restart the terminal for the new $PATH value to take effect. You'll be able to type `code .` in any folder to start editing files in that folder.

## That's it

You are ready for the workshop. If you want to build your environment early, just open the repo folder is VS Code and press the button that asks if you want to **Reopen in Containers**. This will build the development image and create a container and place you in it.

[Back](../README.md)
