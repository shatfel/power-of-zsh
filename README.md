# power-of-zsh

А ващЬ `bash` так могёт???))))))

## Файлы

1. [net.conf](pre/net.conf) - конфиг
2. [net-up](pre/net-up) - настройка сети
3. [host-config](pre/host-config) - настройка /etc/hosts
4. [create-md-log](pre/create-md-log) - генерация примеров ниже.
## Примеры

### `forceDelete=false ./net-up`


#### `ifconfig -a|grep tap`

```shell
tap0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
tap1: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500

```

```shell
/i/ loading config  ./net.conf .. 

/i/ configuring interface tap0
/i/ looks line interface tap0 already configured .. checking for deleting .. 
/i/ stay interface tap0 as is .. 

/i/ configuring interface tap1
/i/ looks line interface tap1 already configured .. checking for deleting .. 
/i/ stay interface tap1 as is .. 
```

### `forceDelete=true ./net-up`


#### `ifconfig -a|grep tap`

```shell
tap0: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500
tap1: flags=4099<UP,BROADCAST,MULTICAST>  mtu 1500

```

```shell
/i/ loading config  ./net.conf .. 

/i/ configuring interface tap0
/i/ looks line interface tap0 already configured .. checking for deleting .. 
/i/ selected force deleting interfaces .. 
/i/ creating interface tap0 .. 
/i/ configuring network on tap0 .. 

/i/ configuring interface tap1
/i/ looks line interface tap1 already configured .. checking for deleting .. 
/i/ selected force deleting interfaces .. 
/i/ creating interface tap1 .. 
/i/ configuring network on tap1 .. 
```

### ` ./net-up`


#### `ifconfig -a|grep tap`

```shell
tap0: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500
tap1: flags=4163<UP,BROADCAST,RUNNING,MULTICAST>  mtu 1500

```

```shell
/i/ loading config  ./net.conf .. 

/i/ configuring interface tap0
/i/ looks line interface tap0 already configured .. checking for deleting .. 
/i/ selected force deleting interfaces .. 
/i/ creating interface tap0 .. 
/i/ configuring network on tap0 .. 

/i/ configuring interface tap1
/i/ looks line interface tap1 already configured .. checking for deleting .. 
/i/ selected force deleting interfaces .. 
/i/ creating interface tap1 .. 
/i/ configuring network on tap1 .. 
```
