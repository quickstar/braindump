# Nginx basic config

### Default config
/etc/nginx/nginx.conf

### Available Sites
/etc/nginx/sites-available

### Enabled Sites
/etc/nginx/sites-enabled

To enable a site just create a symlink from the config file within sites-available to sites-enabled.
```sh
ln -s /etc/nginx/sites-available/example /etc/nginx/sites-enabled/example
```

To disable a site 
```sh
unlink /etc/nginx/sites-enabled/example
```

To install nginx in arch linux see the official [installation guide](https://wiki.archlinux.org/index.php/nginx).
