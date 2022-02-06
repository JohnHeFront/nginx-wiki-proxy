# nginx-wiki-proxy
维基媒体nginx反向代理

demo
[wikim.tk](http://wikim.tk)

nginx编译参数
（需要`ngx_http_substitutions_filter_module`模块）
```
nginx version: nginx/1.21.6
built by gcc 7.5.0 (Ubuntu 7.5.0-3ubuntu1~18.04)
built with OpenSSL 1.1.1  11 Sep 2018
TLS SNI support enabled
configure arguments: --add-module=/root/ngx_http_substitutions_filter_module --with-http_stub_status_module --with-http_ssl_module --with-http_v2_module
```

启动nginx参数
```
/usr/local/nginx/sbin/nginx -s stop
/usr/local/nginx/sbin/nginx -tc /etc/nginx/conf.d/wiki.conf
/usr/local/nginx/sbin/nginx -c /etc/nginx/conf.d/wiki.conf
```

`wikidomainForSSL.txt`为维基全站申请SSL证书

`wikipedia.conf`只反向代理Wikipedia（所有语言）
