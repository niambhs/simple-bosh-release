# simple-bosh-release
This is a very basic bosh release that delivers a simple ruby file. 
## Approach taken
The following document outlines the approach I took in creating my own release.
I started out reading https://bosh.io/docs/create-release.html. This was really good, as the creation of the release was on going, but not for my first read. [This](http://www.starkandwayne.com/blog/your-first-bosh-release/) blog by Starke and Wayne 
provided the right level of information on how to proceed. 


  2. The link above provided the context for https://github.com/cloudfoundry/bosh-lite 
-	I installed Vagrant https://www.vagrantup.com/docs/getting-started/
-	I installed my virtual box from https://www.virtualbox.org/wiki/Downloads 
-	Downloaded Ruby Mine
-	I created my first ever Ruby class! 
-	I added my class on to my git repository https://github.com/niambhs/RubyRepo.git
-	So, first question how do I connect my bosh release to the source in my git repo?
  1. This was not overtly intuitive (highly probable that I was at fault here!) 
  2. Following the instructions in [add the sources](https://github.com/georgethebeatle/simple-bosh-release/blob/master/README.md#add-the-sources)
  3. I ran  ``` mkdir myRubyCode  ``` 
  4. But the the workspace was not commited to git, installing bash lite I installed to a workspase in my directory instead of under git. 
  5. So I copied the workspace to git (Doh!!)
 -	So, second problem - build artifcats, how do I get these in to my simple bosh release?
    1. Where do my build artifacts reside? 
    2. When in Ruby, we create Gem Files! 
    3. Many attempts were made to create Gem files and the awakening of my family meant I abandoned Ruby! The reason was, compiling code was not the priority, 
       generating a built artifact was! So, I moved on to produce a simple Java file. 


