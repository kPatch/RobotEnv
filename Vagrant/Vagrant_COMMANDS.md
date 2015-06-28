# Vagrant Commands and Configuration

## Up and Running

###Initialize Vagrant by specifying a box
$ `vagrant init precise64 http://files.vagrantup.com/precise64.box`

###Run Vagrant
$ `vagrant up`

At this point Vagrant will be running a VBoxHeadless, a headless version of Virtual Box. That means Virtual Box without a graphical user interface (GUI).
In this case, after these commands finish running, an isolated, fully featured 64-bit Ubuntu 12.04 LTS virtual machine will be runnning in the background.

###Drop into the the virtual machine using SSH

$ `vagrant ssh`

After SSHing into the virtual machine, you can verified the shared files between the virtual machine and the host machine

$vagrant@precise64:~$ `ls /vagrant`

You should see the `Vagrantfile` listed.

The Vagrantfile in that directory is actually the same Vagrantfile in from the project directory in your host machine. If a file is created on the host machine or within the Vagrant machine (virtual machine), the changes will be mirrored from host to guest and vice versa.

The location of the default shared folder can be overriden from the Vagrant file:

`config.vm.synced_folder "../data", "." `

The first parameter "../data" is the path where the folder will exist in the guest machine. This path will be created if it doesn't exist. If it does already exist, the location will be replaced with the contents of the shared folder.

The second parameter "." is the path of the folder to be shared from the host machine. This can be an absolute or relative path. It it is relative, like the example above, it is relative to the project root. So in the example above it is sharing the project root.

Open the Vagrantfile to view other configurations.

###Check the state of the vagrant machine

$ `vagrant status`


##Teardown

###Suspend a virtual machine
When you suspend a machine Vagrant will cache the current state of the machine and can be resumed from this exact suspended state.

The main benefit of suspending a vagrant machine is the ability to resume your work fast. But this comes at the cost of consuming memory on the host machin which will cache the vagrant machine's state.

Suspending a vagrant machine is similar to putting your machine to sleep

$ `vagrant suspend`

###Halt a virtual machine

Halting a vagrant machine is similar to shutting down your machine.
Vagrant will first attempt to gracefully halt the machine. If Vagrant is unable to gracefully shut down the machine, it will forcefully shut it down.
The benefit of the halting a Vagrant environment is the preservation of the machine without taking up no runtime resources on the host machine.

Unline suspending, RAM is not preserved. Since the machine is fully shut down you'll have to make sure any necessary processes such as web servers and dbs are started again.

Similar to suspending, the guest machine continues to consume hard drive space. Depending on the guest machine the can range from 2GB to more than 10GB.

$ `vagrant halt`

###Destroy a virtual machine

As the names says, destroy will "destroy" or remove all traces of the guest machine by deleting hard disks, state files, and so on.

Desstroying a guest machine will cause you to lose any changes made to the machine while it was running.

$ `vagrant destroy`

