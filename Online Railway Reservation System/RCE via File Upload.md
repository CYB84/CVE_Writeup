### Online Railway Reservation System - File upload RCE (/admin/emp-profile-avatar.php)

Vendor Homepage:

https://codeastro.com/online-railway-reservation-system-in-php-with-source-code/

V1.0
Tested on:

PHP, Apache, MySQL
Affected Page:

/admin/emp-profile-avatar.php

## Steps To Reproduce
1. Navigate to the following URL of the Online Railway Reservation System:   Url : http://localhost/ORRS-PHP/admin/emp-profile-avatar.php

2. Upload a malicious web shell (e.g., a `.php` file containing shell commands).

3. Access the uploaded file through the URL:  http://localhost/ORRS-PHP/admin/assets/img/profile/web.php

4. Use the web shell to execute commands on the server. [For Example: dir ]

Proof of vulnerability:
![1](https://github.com/user-attachments/assets/1df26fde-30cd-4c6b-86c6-fa4b7d515868)

![2](https://github.com/user-attachments/assets/c066822c-7952-4065-90b9-f12d91928625)

![3](https://github.com/user-attachments/assets/048d579d-b232-4d31-bc51-24dd66d6e74c)

![4](https://github.com/user-attachments/assets/e9086fed-4dfa-49ca-b49b-688d0df555b8)

![5](https://github.com/user-attachments/assets/96ec7df0-2f82-4a45-997c-3549c771ab04)

![6](https://github.com/user-attachments/assets/197c135d-8189-44c3-85d1-fc96c60a04e0)
