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
t1

After installation, you can view that the command is successfully executed

t2
