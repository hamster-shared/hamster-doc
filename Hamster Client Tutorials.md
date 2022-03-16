# Hamster Client

# 1. Overview

> Hamster Client is used to provide users with the ability to purchase and manage connections to their purchased resources . This includes the Marketplace, My Orders and My Resources modules.

# 2. Run

Download the appropriate version of the client for your system through our [distribution](https://github.com/hamster-shared/hamster-client/releases), or download the source code from [github](https://github.com/hamster-shared/hamster-client) to compile and run.

# 3. How to use

### 3.1 import account

The first time you enter into the client, you need to import your account, as shown in the figure

![image-20220228151452987](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220228151453.png)





### 3.2 Setting

In the settings, you can configure your own public key information, configure the chain node you want to connect to (default is ws://127.0.0.1:9944), you can modify it to the corresponding ip+port number, and you can also set the gateway you want to connect to

![image-20220309171309170](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220309171309.png)

### 3.3 Resource Market

You can view and buy all the resources now available in the 'Resource Market', and enter your public key and duration of your purchase.

![image-20220309154957770](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220309154957.png)

### 3.4 Order List

After the purchase is completed, you can check your order information in 'Order List', and the order status are: Completed, Cancelled, and Processing.

- Completed: The provider has processed the order and is ready to provide the machine for you to connect.
- Processing: The provider is preparing the machine for your purchase.
- Cancelled: If the processing is not completed for a long time, you can cancel this order and purchase again

![image-20220309154745304](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220309154745.png)





### 3.5 My Resource

Once the order has been processed, you can find all the resources you purchased here

![image-20220309155048989](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220309155049.png)



### 3.6 Link

You can connect your purchased resources here, click connect, then initialize the configuration, enter the port you want to map to the local machine, click link, then you can check the status to see if the connection is successful. 	

Then click copy and execute the command on the command line to connect successfully.

![image-20220309155148546](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220309155148.png)

![image-20220309155205099](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220309155205.png)![image-20220309155215376](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220309155215.png)



### 3.7 Status

![image-20220316172905858](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220316172906.png)

You can copy the ssh command to the command line and run it to access the purchased container
