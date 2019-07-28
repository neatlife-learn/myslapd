## slapd

docker run：

 - `LDAP_DOMAIN`设置LDAP根域。 （例如，如果你提供`foo.bar.com`
  在这里，您的目录的根将是`dc = foo，dc = bar，dc = com`）
 - `LDAP_ORGANISATION`为您的组织设置人类可读的名称（例如
  `Acme Widgets Inc.`）
 - `LDAP_ROOTPASS`设置LDAP管理员用户密码（即密码）
  `cn = admin，dc = example，dc = com`如果你的域是`example.com`）

（可选）您可以配置以下选项：

 - `SLAPD_NOFILE_SOFT`将打开的文件softlimit设置为（默认为系统限制或16,384，取较小者）

```shell
docker-compose up -d
```

```shell
    ldapadd -h localhost -p <host_port> -c -x -D cn = admin，dc = mycorp，dc = com -W -f data.ldif
```
