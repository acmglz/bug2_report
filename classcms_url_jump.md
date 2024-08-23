#### BUG_AUTHOR:acmglz
# The Classcms contains any url jump
## Download address:
https://github.com/ClassCMS/ClassCMS/releases/tag/v4.8
## Version:V4.8
## Tested on: PHP, Apache, MySQL
## Affected Page:
In the background of the column > Application Management > Default Template > Column > Article > Any addition > Modify

1. It is often used for fishing, fraud and other purposes.

2. Break some common security restrictions based on the "whitelist mode".

3. By jumping to collect data and then further dig deeper vulnerabilities.

## Proof of vulnerability:
## Payload：
```
<meta http-equiv="refresh" content="3,http://www.baidu.com"/>
```
## Trigger popup：
![image](https://github.com/user-attachments/assets/00560de8-7a4f-48a0-b494-48afad48e2fe)


Then click to visit the page to trigger

![image](https://github.com/user-attachments/assets/b12195b6-2090-4bc2-ae4d-d36b6da66a1f)

