./logstash-7.17.5/bin/logstash -f niryehoshua.conf --log.level trace --config.debug --config.reload.automatic --config.test_and_exit

root@app:/etc/nginx/sites-available# sudo add-apt-repository ppa:certbot/certbot
PPA publishes dbgsym, you may need to include 'main/debug' component
Repository: 'deb https://ppa.launchpadcontent.net/certbot/certbot/ubuntu/ jammy main'
Description:
The PPA has been DEPRECATED.

To get up to date instructions on how to get certbot for your systems, please see https://certbot.eff.org/docs/install.html.
More info: https://launchpad.net/~certbot/+archive/ubuntu/certbot
Adding repository.
Press [ENTER] to continue or Ctrl-c to cancel.
Found existing deb entry in /etc/apt/sources.list.d/certbot-ubuntu-certbot-jammy.list
Adding deb entry to /etc/apt/sources.list.d/certbot-ubuntu-certbot-jammy.list
Found existing deb-src entry in /etc/apt/sources.list.d/certbot-ubuntu-certbot-jammy.list
Adding disabled deb-src entry to /etc/apt/sources.list.d/certbot-ubuntu-certbot-jammy.list
Adding key to /etc/apt/trusted.gpg.d/certbot-ubuntu-certbot.gpg with fingerprint 7BF576066ADA65728FC7E70A8C47BE8E75BCA694
Hit:1 http://mirrors.digitalocean.com/ubuntu jammy InRelease
Hit:2 http://mirrors.digitalocean.com/ubuntu jammy-updates InRelease
Hit:3 https://artifacts.elastic.co/packages/7.x/apt stable InRelease
Hit:4 http://mirrors.digitalocean.com/ubuntu jammy-backports InRelease
Ign:5 https://ppa.launchpadcontent.net/certbot/certbot/ubuntu jammy InRelease
Hit:6 http://security.ubuntu.com/ubuntu jammy-security InRelease
Hit:7 https://repos.insights.digitalocean.com/apt/do-agent main InRelease
Err:8 https://ppa.launchpadcontent.net/certbot/certbot/ubuntu jammy Release
  404  Not Found [IP: 185.125.190.52 443]
Hit:9 https://repos-droplet.digitalocean.com/apt/droplet-agent main InRelease
Reading package lists... Done
E: The repository 'https://ppa.launchpadcontent.net/certbot/certbot/ubuntu jammy Release' does not have a Release file.
N: Updating from such a repository can't be done securely, and is therefore disabled by default.
N: See apt-secure(8) manpage for repository creation and user configuration details.
W: Target Packages (main/binary-amd64/Packages) is configured multiple times in /etc/apt/sources.list.d/elastic-7.x.list:1 and /etc/apt/sources.list.d/elastic-7.x.list:2
W: Target Packages (main/binary-all/Packages) is configured multiple times in /etc/apt/sources.list.d/elastic-7.x.list:1 and /etc/apt/sources.list.d/elastic-7.x.list:2
W: Target Translations (main/i18n/Translation-en) is configured multiple times in /etc/apt/sources.list.d/elastic-7.x.list:1 and /etc/apt/sources.list.d/elastic-7.x.list:2
W: Target CNF (main/cnf/Commands-amd64) is configured multiple times in /etc/apt/sources.list.d/elastic-7.x.list:1 and /etc/apt/sources.list.d/elastic-7.x.list:2
W: Target CNF (main/cnf/Commands-all) is configured multiple times in /etc/apt/sources.list.d/elastic-7.x.list:1 and /etc/apt/sources.list.d/elastic-7.x.list:2
W: https://repos.insights.digitalocean.com/apt/do-agent/dists/main/InRelease: Key is stored in legacy trusted.gpg keyring (/etc/apt/trusted.gpg), see the DEPRECATION section in apt-key(8) for details.
W: Target Packages (main/binary-amd64/Packages) is configured multiple times in /etc/apt/sources.list.d/elastic-7.x.list:1 and /etc/apt/sources.list.d/elastic-7.x.list:2
W: Target Packages (main/binary-all/Packages) is configured multiple times in /etc/apt/sources.list.d/elastic-7.x.list:1 and /etc/apt/sources.list.d/elastic-7.x.list:2
W: Target Translations (main/i18n/Translation-en) is configured multiple times in /etc/apt/sources.list.d/elastic-7.x.list:1 and /etc/apt/sources.list.d/elastic-7.x.list:2
W: Target CNF (main/cnf/Commands-amd64) is configured multiple times in /etc/apt/sources.list.d/elastic-7.x.list:1 and /etc/apt/sources.list.d/elastic-7.x.list:2
W: Target CNF (main/cnf/Commands-all) is configured multiple times in /etc/apt/sources.list.d/elastic-7.x.list:1 and /etc/apt/sources.list.d/elastic-7.x.list:2


sudo apt-get update

sudo apt-get install python3-certbot-nginx

sudo certbot --nginx certonly
c
If you really want to skip this, you can run the client with
--register-unsafely-without-email but you will then be unable to receive notice
about impending expiration or revocation of your certificates or problems with
your Certbot installation that will lead to failure to renew.

Enter email address (used for urgent renewal and security notices)
 (Enter 'c' to cancel): c
An e-mail address or --register-unsafely-without-email must be provided.
Ask for help or search for solutions at https://community.letsencrypt.org. See the logfile /var/log/letsencrypt/letsencrypt.log or re-run Certbot with -v for more details.
root@app:/etc/nginx/sites-available#

