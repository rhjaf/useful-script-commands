
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
