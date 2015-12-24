安装composer
-----------

 * linux安装很简单，很方便，同时没有遇到太大的问题（这里略过）
 * 主要是windows ，windows 上面需要安装ca证书，否则会出错，错误如下：
     [Composer\Downloader\TransportException]
     The "https://packagist.org/packages.json" file could not be downloaded: SSL
      operation failed with code 1. OpenSSL Error messages:
     error:14090086:SSL routines:SSL3_GET_SERVER_CERTIFICATE:certificate verify
     failed
     Failed to enable crypto
     failed to open stream: operation failed
     这是由于缺少ca证书导致的，需要下载证书[链接地址][href]: <http://curl.haxx.se/docs/caextract.html>
     同时修改php.ini文件如下：
    openssl.cafile= D:/wamp/php/verify/cacert.pem
    再次运行就正常了
 
