# hamster-doc

If you want to test hamster in its entirety, you must have the following three components.

- chain node: it needs to be deployed on a machine with a public ip
- provider
- client

The following is the minimum test procedure, for a full description please go to the README or tutorial of each project



## 1. Start hamster node

First you need to start a test chain node (please ensure that he is running on a machine with a public IP).

docker is the easiest way to run, we recommend using docker for building Hamster nodes

Points to note before run in docker：

- You need to install [docker](https://www.docker.com/) by yourself before starting, refer to docker official website for details

* You can choose to run your own test node with Docker. The start command is as follows, where <YourDataDir> is your local directory address, <YourNodeName> is your node name 

```bash
docker run -p 30333:30333 -p 9944:9944 -p 9933:9933 --restart=always -d -v <YourDataDir>:/tmp/db --name=hamster hamstershare/hamster:v1.0.0 /opt/ttchain/node-template --dev --name <YourNodeName> --ws-external --rpc-external --rpc-cors all --unsafe-rpc-external --rpc-methods unsafe --unsafe-ws-external --no-mdns
```

You can check if the container is running properly by using the following command:

```bash
docker logs -f hamster
```

![image-20220316165302793](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220316165303.png)

## 2. Register for Resources

Before registering for resources, please ensure that you have created an account and that it has a sufficient balance, please refer to [Create an account](https://github.com/hamster-shared/hamster-doc/blob/main/Hamster%20Chain%20Tutorials.md#3-create-an-account)

Once registered, start the provider process on the computer you wish to rent out, please refer to [Hamster Provider Tutorials](https://github.com/hamster-shared/hamster-doc/blob/main/Hamster%20Provider%20Tutorials.md#2-run) for the start-up process，then visits[provider](http://localhost:3100)

![image-20220222164333091](https://gitee.com/lzw657434763/pictures/raw/master/Blog/20220316170723.png)

Change the address in the corresponding chainAddree to your chain address, account to your account helper, select cpu, memory, boot method and other information and click update.

Before renting the machine, you must pledge a certain amount, otherwise the order will fail to be executed, the pledge must meet the order amount of 1:1, you can play as pledge in "account information"

When the above operation is completed and confirmed, come to the "boot" and click start, then go to "Resource Details" to change your price, at last you can view your rental resources in the calculation market. 

## 3. Purchase and use resources

Download the appropriate version of the client for your system through our [distribution](https://github.com/hamster-shared/hamster-client/releases)

Once downloaded, please refer to [Hamster Client Tutorials](https://github.com/hamster-shared/hamster-doc/blob/main/Hamster%20Client%20Tutorials.md#3-how-to-use) to purchase and use the resources

Note: A certain amount of token must also be in the account, please refer to [Transfer](https://github.com/hamster-shared/hamster-doc/blob/main/Hamster%20Chain%20Tutorials.md#3-create-an-account) for the process. create-an-account)

