
instalasi suricata
instalasi suricata tetap menggunakan ```root``` dengan menggunakan command
```Sudo apt install Suricata ```
lalu instalasi dapat di cek apakah sudah berjalan menggunakan ```sudo systemctl status suricata```
```
 suricata.service - LSB: Next Generation IDS/IPS
     Loaded: loaded (/etc/init.d/suricata; generated)
     Active: active (running) since Wed 2021-12-01 15:54:28 UTC; 2s ago
       Docs: man:systemd-sysv-generator(8)
    Process: 1452 ExecStart=/etc/init.d/suricata start (code=exited, status=0/SUCCESS)
      Tasks: 12 (limit: 9513)
     Memory: 63.6M
     CGroup: /system.slice/suricata.service
             └─1472 /usr/bin/suricata -c /etc/suricata/suricata.yaml --pidfile /var/run/suricata.pid -q 0 -D -vvv

Dec 01 15:54:28 suricata systemd[1]: Starting LSB: Next Generation IDS/IPS...
Dec 01 15:54:28 suricata suricata[1452]: Starting suricata in IPS (nfqueue) mode... done.
Dec 01 15:54:28 suricata systemd[1]: Started LSB: Next Generation IDS/IPS.
```
jika suricata sudah running maka instalasi selesai
