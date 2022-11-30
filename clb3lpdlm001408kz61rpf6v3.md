# Traverxec

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1669810003368/A9rJg3v7-.png align="left")

1.  使用 Nmap 扫描
    
    ```bash
    nmap -sT --min-rate 1000 -p 1-65535 10.10.10.165
      PORT   STATE SERVICE
      22/tcp open  ssh
      80/tcp open  http
    nmap -sTCV --min-rate 1000 -p 22,80 10.10.10.165
      PORT   STATE SERVICE VERSION
      22/tcp open  ssh     OpenSSH 7.9p1 Debian 10+deb10u1 (protocol 2.0)
      | ssh-hostkey: 
      |   2048 aa:99:a8:16:68:cd:41:cc:f9:6c:84:01:c7:59:09:5c (RSA)
      |   256 93:dd:1a:23:ee:d7:1f:08:6b:58:47:09:73:a3:88:cc (ECDSA)
      |_  256 9d:d6:62:1e:7a:fb:8f:56:92:e6:37:f1:10:db:9b:ce (ED25519)
      80/tcp open  http    nostromo 1.9.6
      |_http-title: TRAVERXEC
      |_http-server-header: nostromo 1.9.6
      Service Info: OS: Linux; CPE: cpe:/o:linux:linux_kernel
    ```