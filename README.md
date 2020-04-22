
# wp-meta-verify
This is a ake plugin to test Travis CI

## Creating repository
```console
$ cd /srv/www/camisetas.codigo.co.uk/current/web/app
$ git clone https://github.com/pablorica/wp-meta-verify
```
## Updating `.travis.ylm`

Original:

```
matrix:
  include:
    - php: 7.2
      env: WP_VERSION=latest
    - php: 7.1
      env: WP_VERSION=latest
    - php: 7.0
      env: WP_VERSION=latest
    - php: 5.6
      env: WP_VERSION=latest
    - php: 5.6
      env: WP_VERSION=trunk
    - php: 5.6 <- Failed build 
      env: WP_TRAVISCI=phpcs
    - php: 5.3 <- Failed build 
      env: WP_VERSION=latest
      dist: precise
``` 
Update:

```
matrix:
  include:
    - php: 7.1
      env: WP_VERSION=latest
    - php: 7.0
      env: WP_VERSION=latest
    - php: 5.6
      env: WP_VERSION=latest
    - php: 5.6
      env: WP_VERSION=trunk
``` 

