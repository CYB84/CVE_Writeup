# Prison Management System
## Directory on `/uploadImage/Profile/`

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
/uploadImage/Profile/
```

The Directory Listing Vulnerability occurs when the web server is configured to allow directory listings. In the case of the Prison Management System (version 1.0), the /uploadImage/Profile/ directory is not properly secured. As a result, any remote attacker can access this directory and view the files stored within it. The files within this directory may contain sensitive information such as user profiles, images, and other confidential data, leading to potential data breaches and unauthorized access.


### Proof of Concept:

![1](https://github.com/user-attachments/assets/2382e66d-5864-4abd-a6ca-45e81618a41a)

![2](https://github.com/user-attachments/assets/41a8043d-3522-4cf1-a879-f856fe8ae082)

### Recommended Mitigation:

To mitigate this vulnerability, the following steps are recommended:

1. Disable Directory Listing: Ensure that directory listing is disabled on the web server. This can typically be done by modifying the server’s configuration file (e.g., .htaccess for Apache or nginx.conf for Nginx).

2. Implement Access Controls: Restrict access to sensitive directories using proper authentication and authorization mechanisms. Only authorized users should have access to the /uploadImage/Profile/ directory.

3. Regular Security Audits: Conduct regular security audits of the application and server configurations to identify and address any potential vulnerabilities.

4. Apply Security Patches: Stay up to date with security patches and updates provided by the application vendor or developer.



