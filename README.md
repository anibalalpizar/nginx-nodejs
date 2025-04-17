# Nginx and Node.js Project

This project demonstrates the use of Nginx as a reverse proxy for a Node.js application. Below are instructions for managing Nginx and generating self-signed certificates.

## Nginx Commands

### Start Nginx

```bash
nginx
```

### Get Options

Display available Nginx options:

```bash
nginx -h
```

### Restart Nginx

Reload the Nginx configuration without stopping the server:

```bash
nginx -s reload
```

### Stop Nginx

Stop the Nginx server:

```bash
nginx -s stop
```

### Print Logs

View the Nginx access logs in real-time:

```bash
tail -f /usr/local/var/log/nginx/access.log
```

## SSL Certificates

### Create a Folder for Nginx Certificates

```bash
mkdir ~/nginx-certs
cd ~/nginx-certs
```

### Create a Self-Signed Certificate

Generate a self-signed SSL certificate valid for 365 days:

```bash
openssl req -x509 -nodes -days 365 -newkey rsa:2048 -keyout nginx-selfsigned.key -out nginx-selfsigned.crt
```

## Additional Information

- Ensure Nginx is installed and properly configured before running these commands.
- Modify the `nginx.conf` file as needed to suit your application's requirements.
- For more details, refer to the [Nginx documentation](https://nginx.org/en/docs/).
