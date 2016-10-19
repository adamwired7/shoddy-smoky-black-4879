# Wired7 Demo

### Summary

The evolution of this open source project will help demonstrate the Wired7 sprint flow.

The first commit is a relatively barebones project start: Vagrant + a Sinatra app with a hello world page.

Over the course of multiple Wired7 sprints (1 sprint = 1 github issue / ticket), this project will eventually leverage at least four different skillsets / frameworks:

- Ember.js for the frontend client
- Sinatra for the backend API service
- RSpec for backend testing
- Chef for server provisioning

Multiple people can and are encouraged to join a single sprint.  The best contribution from each sprint will be selected for merge into this project.

Feel free to join any active sprints for this project through Wired7.com.


### Setup

We have wrapped Vagrant around this project to make setup and running the application in an isolated environment painless.  

Provision a virtual machine using Vagrant (https://www.vagrantup.com/downloads.html -- you will probably want Vagrant to work through VirtualBox https://www.virtualbox.org/wiki/Downloads)

    vagrant up

This will execute a script that installs rvm as part of the standard provision process.


### Running

Login to the provisioned virtual machine

    vagrant ssh

Change into the application directory

    cd ~/wired7-vm

Install ruby packages

    bundle install

Start the application on port 4567

    ruby lib/sinatra.rb -o 0.0.0.0

Navigate to http://192.168.12.34:4567/ in your browser
