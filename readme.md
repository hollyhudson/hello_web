# Hurdles

- You're laptop isn't on all the time.
- Internet security is hard, best not to invite the internet onto your desktop.
- You probably don't have a static IP at home (unless you have a business account).
- And you could use a hosting service, but then you limit your flexibility and you'll be beholden to their terms of service.
- So you probably want to rent space on a cloud server.
- And then you need to ssh to it to administer it.
- Which means learning ssh.
- And servers run Linux, so you'll need to be comfortable on the command line
- And you have to register a domain.
- And then connect that domain to the static IP of your server instance.
- And you'll probably want to use github to move your actual project around.

OMG!  No wonder webdev classes tend to skip this step.

# UNIX Time!

## Grab the example code

Go to [url] and unpack the zip file where ever you want your project to live.

## Navigation

Open a terminal.  

![Terminal icon](images/terminal_icon.png)


# Github

## Create a new repo

Click "New Repositor" on our github home page.  Do Not initialize
with a readme.

================ unsorted below ==========

Define *server* and *instance* and *cloud*.

generate an ssh key

run ssh-keygen
agree
enter a password (you will type this a lot).

ssh-add

unlocks the key and caches it with a program called ssh-agent.  It
runs all the time in the background.
Why?  So we don't have to keep typing it in for a while.
If you are prompted for a password, run it again to cache the key
for a while again.  How long it caches it depends the operating
system, certain settings, etc.  Look it up if you want to change
things.

Look inside the .ssh directory.  Keep the id_rsa file secret, never
publish it or push it to github, etc.

cat id_rsa.pub and copy paste the contents of the file to github
Can also cat [filename] | pbcopy

Goto add new ssh key on github and paste the contents of the file
in (and note link to more ssh tutorials below the ssh list).

[add thing about finding hex value of key, from screenshot]

Do this prcedure on each machine you work on.  Generating new keys
for each machine means that if a laptop is stolen you can revoke
the key for that laptop in github.

Conceptually, the key is tied to the machine, not to the service.
So you will have one ssh key for, say, your laptop, and use it
whenever you want to use ssh from that machine, whether to push to
github or to log into your instance.

buy an instance
ssh to the instance
as root create a webserver
create a user account
set up the ssh key for the user
	copy the public key into the authorized users file
log out
log in as the user
clone the repo
view the page via the ip address
	- Role of DNS
Register a domain name with domains.google
and associate your instance

DONE!

Choices:
	deeper ssh discussion
	let's encrypt


Recovery process if you lose your ssh key:
	give up your instance
	set up a new instance
	check out your github repo again

Security:
	make your github repo private
