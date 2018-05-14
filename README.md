# swoole聊天室
基于swoole的聊天室，供学习用，支持在线体验：http://chat.ragonli.com/

体验环境：
***
*  php       5.6.33
*  swoole    1.10.4

# 安装
php大于7.0通过pcel安装：
`pecl install swoole`

php小于7.0编译安装：
``` 
wget http://pecl.php.net/get/swoole-1.10.4.tgz
tar zxvf  swoole-1.10.4.tgz
cd swoole-1.10.4
phpize
./configure --enable-sockets --enable-openssl --with-php-config=/usr/local/php/bin/php-config --enable-swoole-debug
make 
sudo make install
```

或到[swoole官网](http://www.swoole.com/)获取安装帮助

# 运行

开启服务：
将目录配置到Nginx/Apache的虚拟主机目录中，使用浏览器访问index.php可访问。 修改`config.php`中，IP和端口为对应的配置。
``` bash
cd /path/to/your/application/
nohup php server.php &
```
