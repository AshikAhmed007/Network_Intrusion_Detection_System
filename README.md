# Network_Intrusion_Detection_System
- "ip a" to get ip and interface name

![2024-02-05 20_22_02-Ubuntu - VMware Workstation](https://github.com/AshikAhmed007/CodeAlpha_Project_Network_Intrusion_Detection_System/assets/44695318/0c0fe225-1dac-4e5c-a50e-d6c35e58636f)

- sudo apt install snort

- cd  /etc/snort/rules
- gedit icmp.rules
alert icmp any any -> 192.168.1.15 any (msg:"ICMP Ping Packet Found";sid:10000001;)

![2024-02-05 20_23_17-Ubuntu - VMware Workstation](https://github.com/AshikAhmed007/CodeAlpha_Project_Network_Intrusion_Detection_System/assets/44695318/0c9ac897-1fe2-484e-b10e-58dbee9a8f80)

- ping 192.168.1.15

![2024-02-05 20_25_21-Ubuntu - VMware Workstation](https://github.com/AshikAhmed007/CodeAlpha_Project_Network_Intrusion_Detection_System/assets/44695318/7d9804d4-d5ef-42b0-9b45-11323a6cd271)

- sudo snort -A console -q -u snort -c /etc/snort/snort.conf -i ens33

![2024-02-05 20_25_47-Ubuntu - VMware Workstation](https://github.com/AshikAhmed007/CodeAlpha_Project_Network_Intrusion_Detection_System/assets/44695318/ca79c8a1-f6e4-468f-9174-603d82ad8ff2)

- 02/05-20:24:24.826514  [**] [1:10000001:0] ICMP Ping Packet Found [**] [Priority: 0] {ICMP} 192.168.1.7 -> 192.168.1.15
- 02/05-20:24:25.829161  [**] [1:10000001:0] ICMP Ping Packet Found [**] [Priority: 0] {ICMP} 192.168.1.7 -> 192.168.1.15
- 02/05-20:24:26.831986  [**] [1:10000001:0] ICMP Ping Packet Found [**] [Priority: 0] {ICMP} 192.168.1.7 -> 192.168.1.15
- 02/05-20:24:27.834961  [**] [1:10000001:0] ICMP Ping Packet Found [**] [Priority: 0] {ICMP} 192.168.1.7 -> 192.168.1.15
