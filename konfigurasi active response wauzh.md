konfigurasi pada ``` /var/ossec/etc/ossec.conf```

bruteforce dan shellshock
```
<!-- Active response firewall-drop scanning -->
<active-response>
  <command>firewall-drop</command>
  <location>all</location> 
  <rules_id> 5763,5712,31168</rules_id>
  <timeout>120</timeout>
</active-response>
 ```
sQLi
```
<!-- Active response firewall-drop scanning -->
<active-response>
  <command>firewall-drop</command>
  <location>all</location> 
  <rules_id> 31103,31170</rules_id>
  <timeout>120</timeout>
</active-response>
 ```
DOS
```
<!-- Active response firewall-drop scanning -->
<active-response>
  <command>firewall-drop</command>
  <location>local</location> 
  <rules_id> 100200,100222</rules_id>
  <timeout>120</timeout>
</active-response>
 ```

penggunaan location dapat digunakan ```all``` jika pemblokiran ingin dilakukna pada semua agent yang wazuh miliki 
sementara itu menggunakan location```local``` jika pemblokiran hanya dilakukan pada tempat kejadian terjadi
