# Stakewars_Challenge13

Migrate validator keys from the MAIN node to the BACKUP node.

We will need a backup server with the same specs that we installed our node. I used 8Vcpu/16Gb ram . First of all install the node like we did before. You can use the link below for installing it. https://github.com/blntbytk/DigitalOcean_SetupRunningValidator 

After finished installing and synching ,connect this new backup server using WinSCP and receive "validator_key.json" , "config.json" and node_key.json" files under ".near" directory under a new directory named as Backup. At my example the name of my file at winSCP is "Node_Yedek_23082022".

![image](https://user-images.githubusercontent.com/105415280/188233285-c19d393e-2b8e-4e41-b9da-dcf6b8710051.png)

Also connect to our main node server using Winscp and receive the same files from it under a new directory named as Main. At my example the name of my file at winSCP s "Node_Ana_23082022"

![image](https://user-images.githubusercontent.com/105415280/188233574-1e4b8f9f-242e-430f-b097-1abbaae1176e.png)


As a summary yyou will see the files like below

![image](https://user-images.githubusercontent.com/105415280/188233809-1bf41715-d676-4579-84a2-c0d73a265f28.png)


Now you are ready for changing the related keys but before it you will have to stop your main node.Use below command for it

systemctl stop neard

Within winscp send the files "validator_key.json" and "node_key.json" at your bacukp directory to the main node server under .near directory


Within winscp send the the files  "validator_key.json" and "node_key.json" at your main directory to the backup node server under .near directory

Thats all now , you main node server becomes backup node server and your backup node server becaomes your main node server.
<img width="948" alt="13_4" src="https://user-images.githubusercontent.com/105415280/188234603-9d4dd49f-d86e-4b22-8ad9-205be6bc0021.PNG">



<img width="945" alt="13_5" src="https://user-images.githubusercontent.com/105415280/188234635-ea225ae5-cbf3-4624-a6c7-927fe53029b6.PNG">







