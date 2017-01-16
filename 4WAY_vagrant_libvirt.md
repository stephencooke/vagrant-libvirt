The following file is the read me idea of what I am trying to create.

A way to run vagrant across four baremetal devices using ssh-managed for admin day to day.

For builds of the actual VMS this takes place native on the LINUX servers running Centos 7.x VM's are mainly el6/el7 

So far  I can four way create things, however the images dont match up and this doesnt work.  The images are not portable and work with bare libvirt. virsh can start/stop.

VAGRANT dont like it!

Create the vagrant image on server1 ,  then hack the files below to make that image work on the others. rsync all from master

$HOME/.vagrant.d/

/etc/libvirtd/qemu

$PROJECT/.vagrant/


Issues found are that images created on one server can not be moved around and vagrant work with them still.  They break and in some instances vagrant will remove the offending image.  Not good if this is your DB Server Client or DNS service.

My understanding of the files below .vagrant.d/ is limited.  I know the actual gems and plugins are best installed native on each server.

boxes  
data  
gems  
insecure_private_key  
plugins.json  
rgloader  
setup_version  
tmp
