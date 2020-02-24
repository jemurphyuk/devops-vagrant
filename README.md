# Environment Variables Lab

## Timings

45 - 60 Minutes

## Summary

We know how to set environment variables and how to persist them between logins by adding them to the bashrc file.

But we're using Vagrant to automatically create environments and we don't want the developers to have to do this manually.

We need to use an environment variable to tell the app the location of the database running on the db VM.

```
mongodb://192.168.10.150:27017/posts
```

## Tasks

* Write a bash command that will inject an export line in to the bashrc
* Use Vagrant a shell provisioner to run this command
* Use your script to create an environment variable called DB_HOST with the correct value for connecting to the database
* Start the app and ensure that the /posts route is now connected correctly

## Bonus

Use ruby to create a method that allows you to easily add more environment variables in the future as needed.

## Tips

the HEREDOC syntax in ruby is a useful way to create big blocks of code as strings.


WEEK 5 DAY 5 NOTES
vagrant up
- closes process of virtual machine being created

user: vagrant
DB_HOST: qa dev
This process closes after the provision
use this information after its been set
How to pass variable from process 1 to process 2 for login in save

vagrant ssh app
- This uses a 'vagrant' user
- Vagrantfile sync app directory to home/ubuntu/app/
- npm install - this is when app is looking for database, seed.js is completed, this is where we need the DB connection
- it will only be to a fixed IP since we have hardcoded it
- va
