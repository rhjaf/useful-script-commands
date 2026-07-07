
1. count the SLOC in your projects ( you can also use [this tool](https://dwheeler.com/sloccount/))
    ```bash
    find . -name '*.c' | xargs wc -l
    ```
2. Search file **content**
    ```bash
    grep -Rn "*test*" .
    ```
3. Search for **filename**
    ```bash
    find . -type f -name "*test*"
    ``` 
4. Network connection issues (Ubuntu)
    ```bash
    systemctl restart NetworkManager
    nmcli networking on
    dhclient -v eth0
    ifconfig eth0 w.x.y.z
    ```
5. Free Memory caches:
    ```bash
    echo 3 > /proc/sys/vm/drop_caches
    ```
6. Replace specific line with SED:
   ```bash
   sed -i '34 s/sum/some/g' Chapter1.txt
   ```
7. Search an application logs via Journallog:
   ```bash
   journalctl -u collectd --since yesterday -n
   ```
8. Set DHCP IP for NIC:
    ```bash
    dhclient etho0 -v
    ```
9. Get Real user, Effective user of a running process:
    ```bash
    ps -eo pid,euser,ruser,comm | grep [process_name]
    ```
10. Connect with a Wireless adapter to a WPA network and get an ip from dhcp 
    ```bash
    iwconfig
    sudo ip link set wlp3s0 up
    sudo wpa_passphrase WLAN_NAME WLAN_PASSWORD > /etc/wpa_supplicant.conf
    wpa_supplicant -i wlp3s0 -c /etc/wpa_supplicant.conf -D wext
    wpa_supplicant -B -i wlp3s0 -c /etc/wpa_supplicant.conf -D wext
    sudo dhclient wlp3s0
    iwconfig
    ```
12. remove packages
    ```bash
    apt-get --purge remove postgresql\*
    rm -r /etc/postgresql/
    rm -r /etc/postgresql-common/
    rm -r /var/lib/postgresql/
    rm -r /var/log/postgresql/
    userdel -r postgres
    groupdel postgres
    ```
