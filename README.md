# iterm2-zmodem

### MacOS

1.安装lrzsz

```
brew install lrzsz
```

2.设置脚本权限

```
chmod 777 /usr/local/bin/iterm2-*
```

3.设置Iterm2的Tirgger特性，profiles->default->editProfiles->Advanced中的Tirgger

```
1.第一条
        Regular expression: rz waiting to receive.\*\*B0100
        Action: Run Silent Coprocess
        Parameters: /usr/local/bin/iterm2-send-zmodem.sh
        Instant: checked
2.第二条
        Regular expression: \*\*B00000000000000
        Action: Run Silent Coprocess
        Parameters: /usr/local/bin/iterm2-recv-zmodem.sh
        Instant: checked
```

### 服务器

安装lrzsz

```sh
yum install lrzsz
```

