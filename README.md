# yellowdns
简单的dns proxy，根据地域转发到不同的dns server，解决访问境外dns的问题

# 使用
直接启动
```
./yellowdns
```
等价于
```
./yellowdns -l :53 -los 114.114.114.114:53 -exs 8.8.8.8:53 -lor CN -lof GeoLite2-Country.mmdb
```
-l：监听的udp地址，默认53

-los: 境内的dns server，默认114.114.114.114:53，域名解析时，先走境内dns server，发现如果是境外ip，则再重新走境外的dns server

-exs：境外的dns server，默认8.8.8.8:53，境外的ip都用这个dns server做解析

-lor: 境内的定义，默认CN

-lof: ip查询国家的数据库文件

其他的选项，参考-h


