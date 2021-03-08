# Ops-generiche
```
Ops Generiche
```

1)apt-get update; apt-get install -y virtualbox git vagrant

2) vim Vagrantfile --> 

Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"
  config.vm.network :forwarded_port, guest: 80, host: 4567
end

cd ~/Vagrant

vagrant up

vagrant ssh default

[vagrant@localhost ~]$ cat /etc/redhat-release 

CentOS Linux release 7.8.2003 (Core)

3) 
