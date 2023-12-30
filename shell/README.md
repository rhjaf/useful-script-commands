
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
