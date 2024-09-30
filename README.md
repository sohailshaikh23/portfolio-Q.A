## Portfolio-Website
Professional Portfolio website

<a href="https://www.oceanofthings.shop" target="_blank">**Visit Now** 🚀</a>


## Web server with SSL certificate

```
sudo apt install nginx
```

Go to your config file here is the location
```
sudo vi  /etc/nginx/sites-available/default
```

add this line in your nginx config file ::  `root /var/www/html` ke neeche and `location /` ke exact upar 
```
server_name oceanofthings.com www.oceanofthings.shop;
```

Now check NGINX config with this command
```
sudo nginx -t
```

Now Restart your NGINX
```
sudo nginx -s reload
```

## Adding SSL certificate to your domain
Now add the certbot repo
```
sudo add-apt-repository ppa:certbot/certbot -y
```

Update your server
```
sudo apt-get update -y
```
```
sudo apt-get install python3-certbot-nginx -y
```
```
sudo certbot --nginx -d oceanofthings.com
```
#-d www.oceanofthings.shop

{This command will ask you some questions like email (provide your email), accept the term and conditions (yes), do `yes` for rest of questions
Only valid for 90 days, test the renewal process with
```
certbot renew --dry-run
```
