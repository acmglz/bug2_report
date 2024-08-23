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
t1

Then click to visit the page to trigger

t2
