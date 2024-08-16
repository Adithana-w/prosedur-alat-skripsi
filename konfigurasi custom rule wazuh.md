aturan pada wazuh dapat ditambahkan melalui wazuh dashboard lalu memilih menu -> management ->rule.
![image](https://github.com/user-attachments/assets/f827cc3e-7b30-4c32-94a1-af00d63633f7)

setelah memilih untuk menambah kedalam manage rules file lalu add new rules files yang diberikan nama ```custom_active_response_rules.xml```. 

![image](https://github.com/user-attachments/assets/08abdd70-3714-46ec-b9e7-5cc52a490314)

aturan 86600 adalah aturan default dari suricata yangmana akan menampilkan setiap alert yang dibuat oleh suricata, pembuatan spesifikasi aturan dengan menyamakan alert dengan command 
```<match> </match> ``` dapat membuat aturan suricata tersebut menjadi aturan baru yang ditantai dengan ```<rule id>```.
