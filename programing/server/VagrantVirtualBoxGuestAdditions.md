Vagrant VirtualBox Guest Additions
==================================
"vagrant-vbguest is a Vagrant plugin which automatically installs the host's VirtualBox Guest Additions on the guest system."
  
Install
-------

```
vagrant plugin install vagrant-vbguest
```
Add config to Vagrantfile
-------------------------

```
Vagrant::Config.run do |config|
  # we will try to autodetect this path. 
  # However, if we cannot or you have a special one you may pass it like:
  # config.vbguest.iso_path = "#{ENV['HOME']}/Downloads/VBoxGuestAdditions.iso"
  # or an URL:
  # config.vbguest.iso_path = "http://company.server/VirtualBox/%{version}/VBoxGuestAdditions.iso"
  # or relative to the Vagrantfile:
  # config.vbguest.iso_path = File.expand_path("../relative/path/to/VBoxGuestAdditions.iso", __FILE__)

  # set auto_update to false, if you do NOT want to check the correct 
  # additions version when booting this machine
  config.vbguest.auto_update = false

  # do NOT download the iso file from a webserver
  config.vbguest.no_remote = true
end
```

_**Reference**_: [https://github.com/dotless-de/vagrant-vbguest](https://github.com/dotless-de/vagrant-vbguest).
