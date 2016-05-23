# thinkphp-php5.6
已安装模块和软件：
  php5-cli
  php5-common
  php5-curl
  php5-dev
  php5-fpm
  php5-gd
  php5-imagick
  php5-json
  php5-mcrypt
  php5-memcache
  php5-memcached
  php5-mysql
  php5-readline
  php5-redis
  php-mongodb-1.1.6(for mongodb3.0)
  rsyslog
  superviosrd
  
# 启动方式：
  docker run -d -p 9000:9000 \
             -v (php-fpm.conf):/etc/php5/fpm/php-fpm.conf:ro \ 
             -v (php.ini):/etc/php5/fpm/php.ini:ro \
             -v (www.conf):/etc/php5/fpm/pool.d/www.conf:ro \
             -v (rsyslog.conf):/etc/rsyslog.conf:ro \
             -v (/data):/data
             andriywzy/thinkphp-php5.6

# 如果不需要rsyslog：
  docker run -d -p 9000:9000 -v .. andriywzy/thinkphp-php5.6 /usr/sbin/php5-fpm -F
  


