# Vagrant

## What is Vagrant

Vagrant is a tool for building complete development environments, sandboxed in a virtual machine.
As Mitchell Hashimoto, founder of Vagrant, expresess in his book, "Vagrant lowers development setup time, increases development/production parity, and brings the idea of disposable compute resources down to desktop".

## Vagrant in Brief

...
Once Vagrant finishes setting up the machine, you are left with a completely sandboxed, fullly provisioned development environment.
Due to the shared folders and networkign, you continue using your own editor and your own browser to develop and test your applications, but the code itself runs on the virtual machine.

Vagrant handles the entire lifecycle of the machine for you.

## Why?


### Installation
The installation and configuration of software on different machines lead to compatibility issues and issues of deploying from a development environement to a production environment.

### Configuration
Misconfiguration of software can lead to functionality that appears to work in development, but does not work the same in production. Manual setup of devlopment environments leads to bugs that don't appear on a developer's machine, but appear in production.

Ideally, what we want is that the development environment mirrors production identically.

### Synchronization
When each developer is responsible for their own, separate, development environment it is difficult to get new members on board and this lead to environments falling out of sync.

### Adoption
It is often difficult for multiple developers to use different operating systems.
Vagrant allows yout to work with the same operating system that is running in production, whether your physical devlopment environment machine is running Linux, Mac OS X, or Windows.

Vagrant puts your development environment into a virtual machine.

## Notes
Working with multiple projects is easy, because each project just gets it's own virtual machine.
All that you need to do is just share the virtual machine image and having new team members build their Vagrant machine with a single command.




 
