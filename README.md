Caddy-Stack
-----------
*PRE-ALPHA SOFTWARE*

Under active development. Not ready for use.

A docker compose file to build 3 containers:

1. Caddy Server
2. PHP
3. MariaDB

Pre-requisites
--------------
1. `SSH` access to server with `sudo` privileges
2. `git`
3. `nano` (or your preferred text editor)
4. `podman`
5. `podman-compose`

There are lots of tutorials on setting up `SSH` access with `sudo` privileges. Use one if you need to get that set up.

If you are using a Fedora-based distro, you can run this command to install the pre-requisite software:
```bash
sudo dnf -y install git nano podman podman-compose
```


Installation
------------
```bash
# Usually in a non-root home user directory (`cd ~`)
cd /path/to/desired/base/directory
git clone https://github.com/jaredhowland/caddy-stack.git
cd caddy-stack
# Edit and save `Caddyfile` to match your needs
nano caddy/Caddyfile
# Edit and save example `.env` to match your needs
nano .env
# Copy your app/website files to this directory
cd websites
podman-compose up --build
```
Copy website files into `/path/to/desired/base/directory/caddy-stack/websites/`

Default MariaDB Information
--------------------------
* **Root User**: `root`
* **Root User Password**: `root-change-me`
* **Regular User**: `admin`
* **Regular User Password**: `change-me`
