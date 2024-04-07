# Pre installed software
## for Mac 
https://docs.docker.com/desktop/install/mac-install/

## Add folder with Magento code
Create folder and add Magento2 code
> /Users/MAC_USER/Developer/m2/

## Add nginx file of Magento app
CLI command in Magento site root
> mv nginx.conf.sample nginx.conf 


## Start/reBuild Docker

> docker-compose up -d --build


## Add Changes to Hosts file
CLI command
> sudo nano /etc/hosts

### Add followings settings for Website Domain
<pre>0.0.0.0 ::1     m.magefast.com</pre>


<br>
<br>


# MySQL

### Host
> db

### Username

> magento

### Password

> magento


### Dbname

> m2

<br>
<br>

# Elasticsearch

### Hostname
> elasticsearch

### Port

> 9200

### Auth

NO
