# Mike's Hacking VM

This is a little play pen to do rough hacks in (or maybe not so rough).  The idea is pretty simple

 Have a nice linux environment to hack in, on whatever host computer I happen to be on.

This is highly opinionated, but the idea itself is so simple anyone could do it...

My favorite linux is openSUSE, so that's the base box used.  After that I just provision whatever common hacking tools I want.

# Mapping directories

I keep my quick-and-dirty hacks in ~/hax/ historically.  The vagrant environment is set up to share the parent host directory to /hax on the VM:

## Example ~/hax directories on the host

 ~/hax                     <---- parent directory
 ~/hax/awk
 ~/hax/blog
 ~/hax/linux-2.6.11.1
 ~/hax/hax-vm              <---- this repository
 ~/hax/some-random-hack

## Same directories shared files on the VM

 /hax                      <---- custom share
 /hax/awk
 /hax/blog
 /hax/linux-2.6.11.1
 /hax/some-random-hack
 /vagrant                  <---- default share (this repo)

# What to include

This is determined by my bootstrap scripts which live in the /bootstrap directory of this repo.  It will probably change and be expanded upon.

I mainly want to install -devel packages for things that I hack with (or on). Also my dotfiles (from my separate dotfiles repo), which I Provision same as I would for any host: clone and then run the `dotfiles` shell script.

That's about it. Details of how it work are very simple, read the Vagantfile and then scripts in /bootstrap
