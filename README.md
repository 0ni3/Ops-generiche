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

3) [vagrant@localhost ~]$ echo "The following providers are enabled: virtualbox, libvirt, hyperv and vmware_desktop (the latter should work for vmware_fusion, vmware_workstation and vmware_desktop)." >> prova.txt


4) [vagrant@localhost ~]$ grep -i "virtual" prova.txt 
The following providers are enabled: virtualbox, libvirt, hyperv and vmware_desktop (the latter should work for vmware_fusion, vmware_workstation and vmware_desktop).

OPPURE -->

[vagrant@localhost ~]$ cat prova.txt | grep -i "virtual"
The following providers are enabled: virtualbox, libvirt, hyperv and vmware_desktop (the latter should work for vmware_fusion, vmware_workstation and vmware_desktop).

5) less prova.txt oppure more prova.txt

6) dentro virtualbox -> settings sulla macchina virtuale creata -> network -> adapter2 -> wlo1

   su nuova console:

   ale@mint ~/Vagrant $ ssh vagrant@192.168.1.215
   The authenticity of host '192.168.1.215 (192.168.1.215)' can't be established.
   ECDSA key fingerprint is SHA256:Xq6hI79G5AN3CSHaw7RcM8d13UAL3hG6ifCerKWYDKw.
   Are you sure you want to continue connecting (yes/no)? yes
   Warning: Permanently added '192.168.1.215' (ECDSA) to the list of known hosts.
   vagrant@192.168.1.215's password: 
   Last login: Mon Mar  8 11:02:59 2021 from 10.0.2.2
   [vagrant@localhost ~]$ 

7) per disabilitare selinux:

   cd /etc/selinux

   ho editato il file config

   SELINUX=disabled
   
   ho fatto il reboot della macchina -->

   [vagrant@localhost ~]$ getenforce
   Disabled
 
   [vagrant@localhost ~]$ sestatus
   SELinux status:                 disabled

8) 
