## Portfolio-Website
Portfolio website build using HTML5, CSS3, JavaScript and jQuery.

<a href="https://www.oceanofthings.shop" target="_blank">**Visit Now** 🚀</a>


## Web server with SSL certificate

```
sudo apt install nginx
```

```
sudo vi  /etc/nginx/sites-available/default
```
add this in your nginx config file
```
server_name oceanofthings.com www.oceanofthings.shop;
```

location / {}

Check NGINX config
```
sudo nginx -t
```

Restart NGINX
```
sudo nginx -s reload
```

```
sudo add-apt-repository ppa:certbot/certbot -y
```

```
sudo apt-get update -y
```

```
sudo apt-get install python3-certbot-nginx -y
```

```
sudo certbot --nginx -d oceanofthings.com -d www.oceanofthings.shop
```

Only valid for 90 days, test the renewal process with
```
certbot renew --dry-run
```
