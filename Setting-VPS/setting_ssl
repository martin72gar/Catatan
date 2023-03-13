On Centos7

- You should have SSL certificate first (Cert & Private Key)
- Generate CSR file to get Cert and Private Key

1. sudo yum install mod_ssl -you
2. Make directory on "/etc/ssl/" to place your SSL Certificate
    - mkdir -p /etc/ssl/"your-domain-name"
    - chmod 700 /etc/ssl/"your-domain-name"
    - cd /etc/ssl/"your-domain-name"
3. Paste or upload your .crt and .key file at that directory
    - nano "your-domain-name".crt
    - nano "your-domain-name".key
    - nano "your-domain-name"ca.crt

4. Add SSL Config on your virtual host conf
    - nano /etc/httpd/conf.d/"your-vhost".conf
    """
    <VirtualHost *:80>

        ServerName www.dewatraining.id

        Redirect “/” “https://martinsiregar.my.id/”

    </VirtualHost>

    <VirtualHost *:443>

        DocumentRoot /var/www/html/public_html/profile

        ServerName www.martinsiregar.my.id

        ServerAlias martinsiregar.my.id

        SSLEngine on

        SSLCertificateFile /etc/ssl/martinsiregar.my.id/martinsiregar.crt

        SSLCertificateKeyFile /etc/ssl/martinsiregar.my.id/martinsiregar.key

        SSLCertificateChainFile /etc/ssl/martinsiregar.my.id/martinsiregar.crt

    </VirtualHost>
    """
5. Test Config
    - sudo apachectl configtest

6. Restart and Testing
    - sudo systemctl restart httpd
    - Try access your domain name


src : https://www.dewaweb.com/blog/tutorial-instalasi-ssl-di-web-server-apache-untuk-centos-7/