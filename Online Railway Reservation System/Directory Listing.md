# Online Railway Reservation System 
## Directory on `/admin/assets/`

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

**Admin Login Details**

Email   : admin@mail.com
Password: codeastro.com

```

### Affected Page:

```
/admin/assets/
```

The Directory Listing Vulnerability occurs when the web server is configured to allow directory listings. In the case of the Online Railway Reservation System (version 1.0), the /admin/assets/ directory is not properly secured. As a result, any remote attacker can access this directory and view the files stored within it. The files within this directory may contain sensitive information such as user profiles, images, and other confidential data, leading to potential data breaches and unauthorized access.


### Proof of Concept:

![1](https://github.com/user-attachments/assets/3ebab503-7786-4642-a91b-45bd810bac62)

![2](https://github.com/user-attachments/assets/a148eb8e-b219-42d4-b93c-8f9838d3db65)



### Recommended Mitigation:

To mitigate this vulnerability, the following steps are recommended:

1. Disable Directory Listing: Ensure that directory listing is disabled on the web server. This can typically be done by modifying the server’s configuration file (e.g., .htaccess for Apache or nginx.conf for Nginx).

2. Implement Access Controls: Restrict access to sensitive directories using proper authentication and authorization mechanisms. Only authorized users should have access to the /uploadImage/Profile/ directory.

3. Regular Security Audits: Conduct regular security audits of the application and server configurations to identify and address any potential vulnerabilities.

4. Apply Security Patches: Stay up to date with security patches and updates provided by the application vendor or developer.



