proxy.conf:

-The server block listens on port 80
-Requests to / (the root path) are routed to the front-end service on port 9000.
-Requests to /api/ are routed to the back-end service on port 5252.
-proxy_pass is used to forward requests to the appropriate Docker service.

/proxy:
build: ./proxy:
                running from folder proxy
ports:"80:80":
                run in local http:localhost
depends_on:
            execute after front-end and back-end
