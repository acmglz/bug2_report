#### BUG_AUTHOR:acmglz
# MiniCMS exists any url jump
## Download address:
https://github.com/bg5sbk/MiniCMS/releases/tag/v1.11
## Version:V1.11
## Tested on: PHP, Apache, MySQL
## Affected Page:
/mc-admin/post-edit.php

1. It is often used for fishing, fraud and other purposes.

2. Break some common security restrictions based on the "whitelist mode".

3. By jumping to collect data and then further dig deeper vulnerabilities.

## Proof of vulnerability:
## Payload：

payload

```
<meta http-equiv="refresh" content="3,http://www.baidu.com"/>
```

## Trigger popup：
![image](https://github.com/user-attachments/assets/c597b9c6-28b9-4f29-92f5-e19a17fae5dc)


Click to view the article to trigger the jump

![image](https://github.com/user-attachments/assets/d61d6fac-485b-4717-9c60-de2ecb848598)

