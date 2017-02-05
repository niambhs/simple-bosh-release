# simple-bosh-release
This is a very basic bosh release that delivers a simple ruby file. 
## Approach taken
The following document outlines the approach I took in creating my own release.
I started out reading https://bosh.io/docs/create-release.html. This was really good, as the creation of the release was on going, but not for my first read. [This](http://www.starkandwayne.com/blog/your-first-bosh-release/) blog by Starke and Wayne 
provided the right level of information on how to proceed. 

However, the best link was cloud foundry's [bosh-lite](https://github.com/cloudfoundry/bosh-lite) documentation. 
## Steps followed
### Preparing the release
1. Install latest version of bosh_cli

```gem install bosh_cli --no-ri --no-rdoc```

2. Install [Vagrant](https://www.vagrantup.com/docs/getting-started/)

3. Downloaded [my virtual box](https://www.virtualbox.org/wiki/Downloads)
3.1 Install version 5.1


4. Clone bosh-lite

 ```cd ~/workspace
$ git clone https://github.com/cloudfoundry/bosh-lite
$ cd bosh-lite```

5. Start Vagrant. 
bin/add-route$ vagrant up --provider=virtualbox```

6. Target the BOSH Director. When prompted to log in, use admin/admin.
```# if behind a proxy, exclude both the VM's private IP and xip.io by setting no_proxy (xip.io is introduced later)
$ export no_proxy=xip.io,192.168.50.4

$ bosh target 192.168.50.4 lite
Target set to `Bosh Lite Director'
Your username: admin
Enter password: *****
Logged in as `admin'```

7. Add a set of route entries to your local route table to enable direct Warden container access every time your networking gets reset (e.g. reboot or connect to a different network). 
```bin/add-route```

### Creating the release.
1. From my github workspace, I ran 
``` bosh init release simple-bosh-release```

### Add content to source directory.
1. I have 2 Java classes, Send.java and Recieved.java from the rabbitmq example.
2. I have also included rabbitmq-server-generic-unix-3.6.6.tar.xz which will be copied over to vm and installed. 

### Generate Job Skeletons
1. Run the following command ```bosh generate job myMessageApp```
2. Update the monit file with start stop commands. 
3. An erb file is created for each job, installing rabbitmq and building the java source and creating the jar file.

**Question** How are jobs ordered?


### rabbitmq
The first thing to do is review the [tutorial](https://www.rabbitmq.com/tutorials/tutorial-one-java.html)
