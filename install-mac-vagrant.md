## install virtual box
download virtual box and install it

## install vagrant
download vagrant and install it

## download a box for ubunto
```
vagrant box add ubuntu/trusty64
```

## edit the Vagrant file

replace
```
config.vm.box = "base"
```
with
```
config.vm.box = "ubuntu/trusty64"
```

## boot the vagrant
```
vagrant up
```
