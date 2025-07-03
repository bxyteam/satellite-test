# <img style="vertical-align:middle; width: 40px; height:40px;" src="https://raw.githubusercontent.com/bxyteam/satellite-test/refs/heads/main/docs/images/terminal.png"> Browxy Instalation

### <img style="vertical-align:middle; width:30px; height:30px;" src="https://raw.githubusercontent.com/bxyteam/satellite-test/refs/heads/main/docs/images/network.png"> Apache2

#### Add configuration file to apache2

```bash 
 sudo bash -c "cat > /etc/apache2/sites-available/browxy_satellites.conf << --EOL
  <VirtualHost *:80>
     RewriteEngine on
     ProxyPreserveHost On
     ServerName satellites.browxy.com
     Redirect permanent / https://satellites.browxy.com/
  </VirtualHost>

  <IfModule mod_ssl.c>
    <VirtualHost *:443>
       RewriteEngine on
       ProxyPreserveHost On
       ServerName satellites.browxy.com
       ProxyPass / http://127.0.0.1:8090/
       ProxyPassReverse / http://127.0.0.1:8090/
       SSLCertificateFile /srv/letsencrypt/live/browxy.com/fullchain.pem
       SSLCertificateKeyFile /srv/letsencrypt/live/browxy.com/privkey.pem
    </VirtualHost>
  </IfModule>
--EOL"
```
* Check server name,  port and SSL certificate paths

#### Link conf file

```bash
  sudo ln -sfn /etc/apache2/sites-available/browxy_satellites.conf /etc/apache2/sites-enabled/browxy_satellites.conf
```

#### Add hostname to hosts file

```bash
  sudo bash -c "printf \"127.0.0.1\tsatellites.browxy.com\n\" >> /etc/hosts"
```

### <img style="vertical-align:middle; width:30px; height:30px;" src="https://raw.githubusercontent.com/bxyteam/satellite-test/refs/heads/main/docs/images/cuboid.png"> Build Docker Image

#### Dockerfile

```Dockerfile
FROM %%DOCKER_REGISTRY%%/browxy_compiler_base:latest

ENV DEBIAN_FRONTEND=noninteractive

# Install dependencies
RUN apt-get update && \
    apt-get install -y sudo dosbox xvfb x11-utils tar gzip xz-utils openjdk-8-jdk locales cron git unzip && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

# grant sudoers privileges
RUN adduser --system --ingroup users --shell /bin/bash --home /home/satellite compiler
RUN echo "compiler ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers
RUN echo "Defaults env_keep+=DOCKER_DAEMON_ARGS" >> /etc/sudoers

# create hosts file and backup
RUN cp /etc/hosts /etc/hosts.default
RUN chmod ugo+rw /etc/hosts.default

RUN mkdir -p /home/satellite/application
COPY ./target/runnable /home/satellite/application
RUN chown -R compiler:users /home/satellite/application
RUN chmod ugo+x /home/satellite/application/*.sh

# Install tini
COPY ./target/runnable/tini /usr/bin/tini
RUN chmod +x /usr/bin/tini

RUN sed -i '/en_US.UTF-8/s/^# //g' /etc/locale.gen && locale-gen
ENV LANG=en_US.UTF-8
ENV LANGUAGE=en_US:en
ENV LC_ALL=en_US.UTF-8

# Set tini as the entrypoint
ENTRYPOINT ["/usr/bin/tini", "--"]

# Set the default command
CMD ["bash", "-c", "/home/satellite/application/dockerStart.sh"]

```
##### Build Image
```bash
docker build -t browxy_satellite .
```

##### Tag Image
```bash
docker build -t docker-registry.beta.browxy.com/browxy_satellite:latest .
```
- ##### Files and folders copied to the image container:
  - dockerStart.sh (start docker application)
  - start.sh (compile and run java application)
  - stop.sh (stop docker application)
  - tini (protects you from software that accidentally creates zombie processes, usefull for dosbox)
  - .env.*
  - /web (web builder folder that contains the files needed to render the HTML page.)

### <img style="vertical-align:middle; width:30px; height:30px;" src="https://raw.githubusercontent.com/bxyteam/satellite-test/refs/heads/main/docs/images/container.png">  Create And Run Docker Container

#### docker-compose.yml

```yaml
version: '2'

services:

  satellite:
    image: docker-registry.beta.browxy.com/browxy_satellite:latest
    env_file:
      - env.prod
    container_name: satellite
    hostname: satellite
    networks:
      - browxy
    restart: unless-stopped
    ports:
      - "8090:8090"
    volumes:
      - /srv/satellite_data:/var/satellite
    ulimits:
      nproc: 524288
      nofile: 524288
# check if need put networks like that
networks:
  browxy:
    external: true

```

### Create And Fill Env File (env.prod)

#### env.prod

```env
# Docker Server port

SERVER_PORT=8090

# Github repository configuration

# github repository name
GITHUB_REPO=

# github repository owner (github username)
GITHUB_OWNER=

# github personal token
GITHUB_TOKEN=

# path to local repository
LOCAL_REPO_PATH=/var/satellite/data/github

# github download repository url (no need for production, replace GITHUB_OWNER and GITHUB_REPO with your credentials)
GITHUB_DOWNLOAD_URL=https://github.com/GITHUB_OWNER/GITHUB_REPO/archive/refs/heads/main.zip

# Spacetrack credentials to update keps and satellite matrix

# spacetrack user credential
SPACE_TRACK_IDENTITY=

# spacetrack password credential
SPACE_TRACK_PASSWORD=

# path to keps files
SATELLITE_KEPS_DIR=/var/satellite/data/github/keps

# web configuration

# name of page builder entry point
ENTRY_POINT=pass

# admin token (only admin)
TOKEN=

# Cron task to update passes (optional default: 1:30)

# Hour 0-23
SCHEDULE_RUN_HOUR=1

# Minute 0-59
SCHEDULE_RUN_MINUTE=30

# Browxy conf

VIRTUAL_HOST=satellites.browxy.com

VIRTUAL_PORT=8090

INSTALL_MODE=browxy

DOCKER_REGISTRY=docker-registry.beta.browxy.com

# configuration ID dev | qa | production
satelliteConfigId=production

```

##### Up Docker Container

```bash
docker-compose up -d
```
