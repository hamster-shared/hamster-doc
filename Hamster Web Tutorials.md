# Hamster Dapp

Hamster Dapp, which allows users to purchase compute resources that have already been provided, and pay a certain Token to purchase a certain amount of time to use the compute resources. We can pay by the hour for more flexible use.



# 1. Run

## 1.1 Docker

docker is the easiest way to build, we recommend using docker for building Hamster nodes

Points to note before run in docker：

- You need to install [docker][https://www.docker.com/] by yourself before starting, refer to docker official website for details

* You can modify the value of BASE_URL by yourself to connect to different underlying chains

```
docker run -d -e BASE_URL=ws://127.0.0.1:9944 -p 80:80 registry.ttchain.tntlinking.com/ttchain/ttchain_frontent_v2:1.0.6
```



# 2. how to use

## 2.1 Link Wallet

First make sure you have the browser wallet plugin [Polkadot{.js} extension](https://polkadot.js.org/extension/) installed.

Then visit the web, choose Link wallet. If you have imported your account in advance in your browser plugin, you will be able to see your account information on dapp

 ```
 http://localhost:80
 ```

![image-20220228105702184](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220228105702.png)



## 2.2 Order Management

Then you can buy resources in dapp or manage your own resource prices, rental times, pledges for your own account, and also view your orders and agreements

![image-20220228111054587](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220228111054.png)



After purchasing the resource, you can check the status of your order in the "order list", if the provider did not execute successfully, you can choose to cancel order to cancel this order

![image-20220228111327965](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220228111328.png)

![image-20220228112033464](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220228112033.png)

View the resources you are using in the service list after the order has been completed

![image-20220228112107425](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220228112107.png)
