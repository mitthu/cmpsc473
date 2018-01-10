# CMPSC 473 (Spring 2018)
We will be using `vagrant` to setup the project environment. This doc will help you get started with `vagrant`. 

## Vagrant
Vagrant is used to automate the setup of virtual environments. We will use the virtualBox backend for the projects. So you will need to install both VirtualBox and Vagrant.

### Installation

* Download and install the appropriate package of VirtualBox: https://www.virtualbox.org/wiki/Downloads
  * If you are using Ubuntu, you can use `sudo apt-get install virtualbox`.
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

### Prepare Environment

This step will speed up the first time initialization process.

* Download the base image of ubuntu from - 
https://vagrantcloud.com/ubuntu/boxes/xenial64/versions/20180105.0.0/providers/virtualbox.box
* Run the following in terminal (or cmd.exe)
```shell
vagrant box add --name "ubuntu/xenial64" <path_to_download>/virtualbox.box
```

### Basic Commands
Download the [Vagrantfile](https://raw.githubusercontent.com/mitthu/cmpsc473_spring18/master/base/Vagrantfile) and save it in your project directory.

* `vagrant up` Use the Vagrantfile in the current directory and setup the development environment. If this command was previously used, then start the previous virtual machine.

* `vagrant ssh` Login to the virtual machine (VM). You should be logged in to the VM and in the `/vagrant` directory. Any files you create/modify/delete in this directory get reflected back in your project directory. The VM should have all the necessary packages installed and configured. Let us know if there is an error - quickest way will be to create an issue on GitHub. 

* `vagrant halt` Stop the virtual machine after work.

* `vagrant destroy` **DESTROY** the VM that was created. You will lose all files created inside the VM. However any files inside the `/vagrant` diriectory will be left untouched.

### FAQs
**Why does it take so long to start?**

The first time you create and setup a project, it will go and download the base image of Ubuntu to bootstrap the OS. This should only happen once. All susequent project setups will reuse the downloaded image.

**What are the resource requirements for the project VM's?**

Each created VM will be given:
- 1 cpu core
- 512 MB RAM
- About 2 GB hard-disk space (will remain even if you `halt` the VM)

**VM fails to boot**

Make sure you are using a 64-bit operaitng system.

