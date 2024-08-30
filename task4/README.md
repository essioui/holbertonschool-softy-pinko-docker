version: '3':
           this version of docker-compose

services:
          define the services that docker compose will manage

          -front-end: => define front-end of projects
                      - build: ./front-end:
                                           * will be use path for create docker image of front-end
                      - ports: "9000:9000":
                                           *ports between container and host (for front-end)
                      - depends_on: back-end:
                                             * docker compose running back-end before execute front-end

          - back-end: => define back-end of projects
                    
                    - build: ./back-end:
                                        * will be use bath for create docker image of back-end
                    - ports: "5252:5252":
                                        * ports between container and host (for back-end)

