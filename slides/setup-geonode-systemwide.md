## Initialize GeoNode systemwide

```bash
$ geonode createsuperuser
# a commandline toolkit has been installed systemwide so let's create the superuser of the GeoNode instance
# use username: 'geonode' and password: 'geonode'
```

```bash
$ sudo geonode-updateip localhost:8888
# update the address where the GeoNode instance is running
$ sudo vi /etc/apache2/ports.conf
# change listen port to 8888
$ sudo vi /etc/apache2/sites-available/geonode.conf
# change the port of virtual host to 8888 and restart
```

**You have installed GeoNode! Congratulations!!!**

Anyway you don't have GeoNode available from your local browser.
So we have to set a new forwarding port in the vagrantfile:

```bash
config.vm.network "forwarded_port", guest: 8888, host: 8888
# This port has to be the same of that before and equal between guest and host. You can understand this later on.
# Again don't use a port lower than 1024 on your host machine (not privileged)!!!
```

After this you have to reload the vagrant configuration:

```bash
$ vagrant reload
# reload vagrantfile with the new configuration
```
