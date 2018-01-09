# CMPSC 473 (Spring 2018)
We will be using `vagrant` to setup the project environment. This doc will help you get started with `vagrant`. 

## Vagrant
Vagrant is used to automate the setup of virtual environments. We will use the virtualBox backend for the projects. So you will need to install both VirtualBox and Vagrant.

### Installation

* Download and install the appropriate package of VirtualBox: https://www.virtualbox.org/wiki/Downloads
* Download and install the appropriate package of Vagrant: https://www.vagrantup.com/downloads.html
  * If you are using Ubuntu, you can use `sudo apt-get install vagrant`.

### Verifying Installation

**Linux:** Open your favorite terminal emulator (command-line console) and type `vagrant help`. If the installation was successful, then a help menu like below will be displayed.
```bash
mitthu@mitthu-laptop ~> vagrant help
Usage: vagrant [options] <command> [<args>]

    -v, --version                    Print the version and exit.
    -h, --help                       Print this help.

Common commands:
     box             manages boxes: installation, removal, etc.
     destroy         stops and deletes all traces of the vagrant machine
     global-status   outputs status Vagrant environments for this user
     halt            stops the vagrant machine
     help            shows the help for a subcommand
     init            initializes a new Vagrant environment by creating a Vagrantfile
     login           log in to HashiCorp's Vagrant Cloud
     package         packages a running vagrant environment into a box
     plugin          manages plugins: install, uninstall, update, etc.
     port            displays information about guest port mappings
     powershell      connects to machine via powershell remoting
     provision       provisions the vagrant machine
     push            deploys code in this environment to a configured destination
     rdp             connects to machine via RDP
     reload          restarts vagrant machine, loads new Vagrantfile configuration
     resume          resume a suspended vagrant machine
     snapshot        manages snapshots: saving, restoring, etc.
     ssh             connects to machine via SSH
     ssh-config      outputs OpenSSH valid configuration to connect to the machine
     status          outputs status of the vagrant machine
     suspend         suspends the machine
     up              starts and provisions the vagrant environment
     validate        validates the Vagrantfile
     version         prints current and latest Vagrant version

For help on any individual command run `vagrant COMMAND -h`

Additional subcommands are available, but are either more advanced
or not commonly used. To see all subcommands, run the command
`vagrant list-commands`.
```

**Mac:** Open the terminal app (/Applications/Utilities/Terminal.app) and type `vagrant help`. If the installation was successful, then a help menu like above (Linux section) will be displayed.

**Windows:** Open cmd.exe (type cmd.exe in the search box of start menu) and type `vagrant help`. If the installation was successful, then a help menu like above (Linux section) will be displayed.
 
