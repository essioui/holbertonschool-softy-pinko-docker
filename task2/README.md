back-end:
          copy of your task1 directory and name it task2.
front-end:
          - clone this repository -> https://github.com/atlas-school/softy-pinko-front-end
          -Dockerfile: + the latest version of nginx.
          -softy-pinko-front-end.conf: 
                    +server{}: open setting of server:
                         *listen 9000; : localhost:9000
                         *server_name localhost; : name of server
                         *location / {}: - use this for URL
                                         -root /var/www/html/softy-pinko-front-end;: path of directory
                                         - index index.html; : this page in localhost:9000

==> after run we have one problem it is "favicon.ico" dont found in path 
