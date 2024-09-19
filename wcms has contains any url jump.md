#### BUG_AUTHOR:acmglz
# wcms has contains any url jump
## Download address:
https://github.com/vedees/wcms/releases/tag/0.3.2
## Version:v0.3.2
## Tested on: PHP, Apache, MySQL
## Affected Page:
/wcms/wex/html.php

payload: 

```
<meta http-equiv=refresh content=2,url=http://www.baidu.com>
```



## Proof of vulnerability:

1. Access: /wcms/






