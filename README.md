# naoki-macos-installer

A easly customisable MacOS script for any new setup. Designed to be used as a pattern to quickly build your own.

*__Good to know :__ It aims to be use for the first admin account of the Mac. If you already have an administrator account on your Mac and use it for a second one, you'll have conflict with file permission, as the system shares things between accounts.*

It installs automatically :

- Xcode
- Git
- Homebrew
- A full configuration of Zsh and Oh My Zsh with the following theme (and more :)

![Zsh theme](https://i.ibb.co/n1qLwgc/Capture-d-cran-2021-11-23-10-06-29.png "zsh theme")

- Some Power fonts for the terminal
- All the softwares you add in the `install_files/homebrew_vars.sh`

*At the moment, a Ruby on Rail and Postgresql setup are present in the project*

- Coming : Preconfigured Mac settings.

You can easily add more, for exemple, dev custom setup by adding a new `.sh` file in `install_files/modules`, and source this file in the `run.sh` file.

Simple :)

## Getting started

After finishing the basic Mac install process :

`curl  -fsSL -H 'PRIVATE-TOKEN: [YOUR_PRIVATE_TOCKEN]' 'https://gitlab.com/api/v4/projects/15401740/repository/archive.zip' -o ~/Documents/mac_dotfiles.zip && cd ~/Documents/ && unzip mac_dotfiles.zip && rm mac_dotfiles.zip`

1. First, download the project and **read the files to custom your setup.** You'll have to do it only once to all your next Mac setup !

2. Open the terminal in the project folder, and run `./run.sh`.

## Customizing the setup

### The architecture

* **install_files** : contain the files used during the installation.
* **modules** : contain the steps (`.sh` files) the script will follow.
* **system_files** contain the files who will be copied to your system.

### The process

* First, the `run.sh` file will load the environment variable.
* Then, it will run each sourced module, if the `.sh` files is present in the `install_files/modules` folder.

That's all. I simply advise you to read all the modules, make it yours, add your modules... and share them to the project !

## Contributors

As I'm not a bash expert, all contributions are wellcome to improve the project, add more modules etc !

Thank you so much!

## License

naoki-macos-installer is released under the GPLv3 license.
