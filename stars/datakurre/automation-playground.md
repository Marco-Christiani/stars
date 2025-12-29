---
repo: datakurre/automation-playground
url: 'https://github.com/datakurre/automation-playground'
homepage: null
starredAt: '2024-12-11T17:05:40Z'
createdAt: '2022-11-25T21:28:27Z'
updatedAt: '2025-01-08T09:43:51Z'
language: Nix
license: NA
branch: main
stars: 3
isPublic: true
isTemplate: false
isArchived: false
isFork: false
hasReadMe: true
refreshedAt: '2025-12-29T17:34:38.774Z'
description: Mostly open source automation playground
tags: []
---

# Open Automation Playground

[View documentation.](https://datakurre.github.io/automation-playground/)

VirtualBox based Vagrant image is available by running `vagrant up` with the following `Vagrantfile:

```ruby
# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "datakurre/automation-playground"

  config.vm.provision "rebuild", type: "shell",
    inline: "sudo nixos-rebuild switch --flake github:datakurre/automation-playground/main#vagrant"

  config.vm.graceful_halt_timeout = 120

  config.vm.provider "virtualbox" do |vb, override|
    vb.gui = true
    vb.memory = 16384
    vb.cpus = 4

    override.vm.provision "remount", type: "shell",
      inline: "sudo mount -t vboxsf vagrant /vagrant -o umask=0022,gid=1000,uid=1000"
  end

end
```
