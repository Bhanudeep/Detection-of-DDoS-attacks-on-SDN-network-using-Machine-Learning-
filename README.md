# Detection-of-DDoS-attacks-on-SDN-network-using-Machine-Learning-
Simulation of SDN  network and generating our own dataset using iperf and hping3 tools. This locally generated dataset is used to train various models and compare their performance. The best performing model is chosen to be deployed on network to monitor traffic and detect DDoS attacks and alert which host is the victim.
I have used RapidMiner tool to rapidly build , train , test and evaluate the performance of of K-NN,SVM,RF and DL. RF has the overall best accuracy. Therefore it is chosen to monitor and detect attacks on our sdn network. 
Read PDF for more information.
SDN network Topology

![Screenshot_20230224_064538](https://user-images.githubusercontent.com/49368483/221187802-1eb88280-0df1-49ad-8a74-c52daa939202.png)

Detecting Normal Traffic

![Screenshot_20230224_064617](https://user-images.githubusercontent.com/49368483/221187833-81e98571-bd85-4b80-9ec7-a103e6f0c349.png)

Detecting DDoS Traffic

![Screenshot_20230224_064633](https://user-images.githubusercontent.com/49368483/221187857-c1599400-2cef-4304-9e2c-6cc246d877eb.png)
