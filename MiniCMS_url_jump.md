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
t1

Click to view the article to trigger the jump

t2
