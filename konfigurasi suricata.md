pada file suricata ```/etc/suricata/suricata.yaml  ```
pada ```HOMENET``` IP dapat diubah sesuai dengan IP yang akan dipantau atau dapat menggunakan netmask
![image](https://github.com/user-attachments/assets/37e67e7b-3df4-4920-8761-f54ba25334f1)

lalu search menggunakan CTRL+W lalu cari ```Af-packet interface ``` ![image](https://github.com/user-attachments/assets/79b45ffb-7215-4372-b0a1-06c5ba0137b3) 
lalu ubah interface sesuai dengan network interface yang akan dipantau bagian ini dapat dilihat menggunakan ```ifconfig``` atau ```IP -a``` 

default path rule dapat diubah dengna mengganti ```/etc/suricata/rules ``` menjadi  ```var/lib/suricata/rules ```
dikarenakan aturan yang digunakan adalah aturan tambahan sendiri makadari itu penambahan aturan dapat dilakukan seperti berikut

![image](https://github.com/user-attachments/assets/786050e8-f5c6-4556-851f-3e2ec3d08bf5)

------------------------------------------------------------------------
penambahan aturan pada suricata dapat dilakukan pada folder ```var/lib/suricata/rules ```. buat file yang bernama local.rules yang berisikan 
untuk deteksi ping
```alert icmp $external_NET any ->$home_net any (msg: "ping someone testing with ping"; itype:8; threshold :type both,track by_src,count 5,seconds 10;sid 1000007;rev:1;) ```
untuk deteksi DOS syn
```alert tcp $external_NET any ->$home_net any (msg: "potential DOS" ;flow:to_server;flags:S.,12;threshold:type both,track by_src count 10000,second 1;classtype:misc-activity;sid:5;)```


