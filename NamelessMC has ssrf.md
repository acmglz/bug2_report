#### BUG_AUTHOR:acmglz
# NamelessMC has ssrf
## Download address:
https://github.com/NamelessMC/Nameless/releases/tag/v2.1.2
## Version:v2.1.2
## Tested on: PHP, Apache, MySQL
## Affected Page:
/index.php?route=/profile/admin/

1. Port scanning and internal network attacks
2. Read and run the local file ‌
3. Access the internal system
4.DOS attack

## Proof of vulnerability:
## Payload：

```
payload: <img src="http://xxx.com/1.png">
```



## Trigger popup：

1, Personal information message, enter ssrfpayload

2, using burp to trigger the test can see the successful trigger

