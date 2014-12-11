# Vagrant with Homestead provisioning

## Why?
Well, I wanted that our developers could easily add new repositories to a vagrant box. We are working multiple projects
at the time and having all projects into one box was not the most easy setup. Also the way homestead is installed is for
our frontend developers not the easiest way.

## So how does it work
Simply clone this repo, copy the following files into your own repo:
- provision/
- Vagrantfile
- Homestead.yaml

## Other documentation
Please install [vagrant-hostsupdater](https://github.com/cogitatio/vagrant-hostsupdater) plugin, as it will be
quite easy to add other aliases to your box.

`$ vagrant plugin install vagrant-hostsupdater`

## Todo:
- I have to edit the serve script so we can add mutliple server_aliases to nginx vhost
- Clean up some stuff