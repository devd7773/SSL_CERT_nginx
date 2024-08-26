-- How to Enable HTTPS in Your Domain Hosted on Linux Remote Server or VPS
--
-- Let's Encrypt is a non-profit certificate authority run by Internet Security Research Group that provides X.509 certificates for Transport Layer Security encryption at no charge.
--
-- Certbot is a free, open source software tool for automatically using Let’s Encrypt certificates on manually-administrated websites to enable HTTPS.
--
--> Install Certbot and it’s Nginx plugin
--
sudo apt install certbot python3-certbot-nginx

-->  Verify Web Server Ports are Open and Allowed through Firewall
--
sudo ufw status verbose

-->  Obtain an SSL certificat
--
sudo certbot --nginx -d your_domain.com -d www.your_domain.com

-->  Check Status of Certbot
--
sudo systemctl status certbot.timer

-->  Dry Run SSL Renewal
--
sudo certbot renew --dry-run






