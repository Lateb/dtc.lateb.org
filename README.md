INSTALLATION
============

Images
------

Add two images named "img/error.jpg" and "img/success.jpg".

Nginx
-----

    server {
    	listen     2014;
    
    	error_log  /var/www/logs/dtc.lateb.org.2014.error.log;
    	error_page   500 502 503 504  /50x.html;
    	location = /50x.html {
    		root  /var/www/htdocs;
    	}
    
    	location / {
    		root    /var/www/2014;
    		rewrite ^/contact$      /contact.html break;
    		rewrite ^/FAQ$          /faq.html break;
    		rewrite ^/success$      /success.html break;
    		rewrite ^/error$        /error.html break;
    	}
    }

CGI
---

TODO
