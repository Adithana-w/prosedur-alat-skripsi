instalasi wazuh dapat dilakukan menggunakan ```root``` user lalu menggunakna komen

```
curl -sO https://packages.Wazuh.com/4.7/Wazuh-install.sh && sudo bash ./Wazuh-install.sh -a 
```

Instalasi berhasil jika di akhir ada pesan seperti ini:

```
INFO: --- Summary ---
INFO: You can access the web interface https://<wazuh-dashboard-ip>
   User: admin
   Password: <ADMIN_PASSWORD>
INFO: Installation finished.
```
setelah itu wazuh dapat diakses melalui ```https://<wazuhIP>```


