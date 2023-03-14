## Lxd Basic Commands
### Port Forwarding

```
lxc config device add c01 proxy0 proxy listen=tcp:172.16.56.208:2222 connect=tcp:10.18.245.33:22
```

### create and mount new volume

`lxc storage volume create default mail-data size=32GB`

`lxc storage volume attach default mail-data mail sdb /mail`

### limit resources

`lxc config set mysql limits.memory 1024MB`

`lxc profile  set default limits.memory 2048MB`

`lxc profile device set  default root size 3GB`

`lxc config set nginx-proxy limits.cpu 2`

### add new nic device
`lxc config device add nextcloud eth6 nic  parent=br6 nictype=bridged`
