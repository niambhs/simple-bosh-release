# simple-bosh-release
This is a very basic bosh release that delivers a simple ruby file. 
## Approach taken
The following document outlines the approach I took in creating my own release.
I started out reading https://bosh.io/docs/create-release.html. This was really good, as the creation of the release was on going, but not for my first read. [This](http://www.starkandwayne.com/blog/your-first-bosh-release/) blog by Starke and Wayne 
provided the right level of information on how to proceed. 

However, the best link was cloud foundry's [bosh-lite](https://github.com/cloudfoundry/bosh-lite) documentation. Once [Vagrant](https://www.vagrantup.com/docs/getting-started/) was installed, 
I downloaded [my virtual box](https://www.virtualbox.org/wiki/Downloads). 
## Steps followed
### Preparing the release
''' git clone https://github.com/cloudfoundry/bosh-lite.git
cd bosh-lite
vagrant up'''


### rabbitmq
The first thing to do is review the [tutorial](https://www.rabbitmq.com/tutorials/tutorial-one-java.html)
