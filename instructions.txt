Find dataset here: https://drive.google.com/file/d/1N2QLDPb90XOdxcuQ_Fb7ZSVOG4J3w_zY/view?usp=sharing


Generating Normal traffic:
run command ryu-manager collect_normal_traffic.py in generate_normal_traffic folder.
run command "service openvswitch-switch start"
run command sudo python generate_normal_traffic.py in generate_normal_traffic folder.
Restart PC:
Generating DDoS traffic:
run command ryu-manager collect_ddos_traffic.py in generate_ddos_traffic folder.
run command "service openvswitch-switch start"
run command sudo python generate_normal_traffic.py in generate_ddos_traffic folder.
Restart PC:

Detecting Attacks and Normal Traffic:
run command service openvswitch-switch start
run command ryu-manager Detection.py in mininet folder. 
run command sudo python SDN.py in mininet folder
after the above command in the same terminal, run command xterm h1 h6 h13 h17.

Normal traffic
ping 10.0.0.15 on node h17 then ping 10.0.0.4 on h6
go to h13 do cd .. ls, clear, git clone, wget etc commands
stop
DDOS traffic:
hping3 is a network tool to perform ddos attacks.
now on node h17 ping 10.0.0.18
on node h6 hping3 -1 -V -d 120 -w 64 -p 80 --rand-source --flood 10.0.0.12 icmp flood
hping3 -S -V -d 120 -w 64 -p 80 --rand-source --flood 10.0.0.12 syn flood
hping3 -2 -V -d 120 -w 64 -p 80 --rand-source --flood 10.0.0.12 udp flood
hping3 -1 -V -d 120 -w 64 -p 80 --rand-source --flood -a 10.0.0.12 10.0.0.12 smurfs
