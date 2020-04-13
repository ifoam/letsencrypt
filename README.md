# letsencrypt
Enable SSL via Let’s Encrypt
Install CertBot (if repo add fails, install software-properties-common)..
$ add-apt-repository ppa:certbot/certbot
$ apt clean all && apt update
$ apt install -y certbot python-certbot-apache
.. certify the domain..
$ certbot --apache -d domain.tld
.. and check the autorenewal is present and working.
$ cat /etc/cron.d/certbot
$ certbot renew --dry-run
