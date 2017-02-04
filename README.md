# simple-bosh-release
This is a very basic bosh release that delivers a simple ruby file. 
## Approach taken
The following document outlines the approach I took in creating my own release.
- I started out reading https://bosh.io/docs/create-release.html.
  1. Too much low level detail on what was required for my first time.
- 	http://www.starkandwayne.com/blog/your-first-bosh-release/.
  1. This was a really good high level blog that got me started on the right track.
  2. The link above provided the context for https://github.com/cloudfoundry/bosh-lite 
-	I installed Vagrant https://www.vagrantup.com/docs/getting-started/
-	I installed my virtual box from https://www.virtualbox.org/wiki/Downloads 
-	Downloaded Ruby Mine
-	I created my first ever Ruby class! 
-	I added my class on to my git repository https://github.com/niambhs/RubyRepo.git
-	So, question how do I connect my bosh release to the source in my git repo?
  1. Following the instructions in [add the sources](https://github.com/georgethebeatle/simple-bosh-release/blob/master/README.md#add-the-sources)
  ``` mkdir myRubyCode  ```




  ``` vagrant up ```
