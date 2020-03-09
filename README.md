# ViaBTC Exchange Server(support websocket)

这个版本做了一下修改

支持docker自动编译viabtc_exchange_server，自己编译viabtc_exchange各种坑
修改了accessws中的config.json，更改svr 的bind 为  tcp:0.0.0.0:8090
解决很多人发现websocket不工作的问题，同时在docker中对外暴露端口也是8090

因此
ws端口对外暴露端口为8090，http为8080
那么ws的访问方式则是 服务器ip:8090

非常注意，如果你采用了阿里clound的ECS或者亚马逊的AWS的服务器，记得在控制台放开安全组策略，这些端口都要防火墙打开允许访问，否则websocket仍然不能工作!!

至于大家问auth_url是否要更改，这个和websocket链接无关系，只是在账户信息授权访问时需要使用，当你建立一个前端程序时，需要提供账户信息授权token令牌，那么此时auth_url是需要更改为你交易所前端程序账户信息授权url的

