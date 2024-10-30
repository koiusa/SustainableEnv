## Set the path of the referenced media file

- If the following error occurs when starting the service, please change the path of the referenced media file to a valid one.

```sh
service "universalmediaserver" refers to undefined volume path/to/yourMediaDir: invalid compose project
```

```txt:docker/ums/.env
MEDIADIR=path/to/yourMediaDir
```

## Setting the network interface to use 

- Please configure the configuration file that is automatically created after starting the service to suit your environment.

```txt:docker/ums/profile/UMS.conf
network_interface=enp2s0
```


