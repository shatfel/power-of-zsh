# power-of-zsh

А ващЬ `bash` так могёт???))))))

[net-up](net-up)

## Примеры

### Удалять, если существует интерфейс и сконфигурировать

```shell
# forceDelete=true ./net-up
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

### Пропустить интерфейс, если существует

```shell
# forceDelete=false ./net-up
/i/ configuring interface tap0
/i/ looks line interface tap0 already configured .. checking for deleting ..
/i/ stay interface tap0 as is ..
/i/ configuring interface tap1
/i/ looks line interface tap1 already configured .. checking for deleting ..
/i/ stay interface tap1 as is ..
```

### И самый наглядный пример

```shell
# forceDelete=false ./net-up
/i/ configuring interface tap0
/i/ creating interface tap0 ..
/i/ configuring network on tap0 ..
/i/ configuring interface tap1
/i/ looks line interface tap1 already configured .. checking for deleting ..
/i/ stay interface tap1 as is ..
```
