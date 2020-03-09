# ViaBTC Exchange Server(support websocket)

这个版本做了一下修改

支持docker自动编译viabtc_exchange_server
修改了accessws中的config.json，解决很多人发现websocket不工作的问题，ws端口对外暴露改为8090，http为8080
那么ws的访问方式则是 服务器ip:8090 
非常注意，如果你采用了阿里clound的ECS或者亚马逊的AWS的服务器，记得在控制台放开安全组策略，这些端口都要防火墙打开允许访问，否则websocket仍然不能工作!!

