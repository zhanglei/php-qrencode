# php-qrencode

基于libqrencode+libgd的生成二维码的php扩展


## 安装:

1，安装libpng & libjpg

sudo apt-get install libpng-dev

sudo apt-get install libjpg-dev

2，安装libqrencode

wget http://fukuchi.org/works/qrencode/qrencode-3.4.4.tar.gz

tar zxvf qrencode-3.4.4.tar.gz

cd qrencode-3.4.4/

./configure

make&make install

3，安装libgd

sudo apt-get install libgd-dev

4，安装php-qrencode

git clone https://github.com/Leon2012/php-qrencode

cd php-qrencode

phpize

./configure

make&sudo make install

5，修改配置文件

vi php.ini

extension=qrencode.so


## 用法:

$resource = qrencode_create("test");

qrencode_save($resource, "/Users/kentchen/Downloads/t3.png");//保存文件

echo qrencode_version()."\n";//查看版本号