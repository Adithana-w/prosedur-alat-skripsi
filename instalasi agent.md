untuk melakukan instalasi pada agent yang pertama lakukan
1. masuk kedalam wazuh melalui browser
2. pilih menu lalu agent
3. setelah informasi agent sudah dimasukan akan muncul code line seperti berikut
```
wget https://packages.wazuh.com/4.x/apt/pool/main/wazuh-agent/wazuh-agent_4.7.2-1_amd64.deb &&
sudo WAZUH_MANAGER='<wazuh IP> WAZUH_AGENT_NAME='<agent name>' dpkg -i ./wazuh-agent_4.7.2-1_amd64.deb

```
code tersebut di pasang pada mesin yang akan dijadikan agent

-------------------------------------------------------------------------------------------------
konfigurasi tambahan untuk suricata

untuk menambahkan suricata log yang akan dilempar kedalam wazuh dapat ditambahkan pada ```/var/ossec/etc/ossec.conf.``` pada mesin suricata dan menambahkan 
![image](https://github.com/user-attachments/assets/281ca988-1707-47dc-bc04-37b8ef8c68e9)
