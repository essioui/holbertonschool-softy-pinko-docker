FROM:
     take latest version of ubuntu

apt-get update:
              download the latest information

apt-get upgrade -y:
                   accept all latest of information
                   -y: that mean yes

RUN apt-get install -y python3 python3-pip:
                    install python3 and python3-pip

RUN rm /usr/lib/python*/EXTERNALLY-MANAGED:
                                        Dont show me message error like latest version of pip3
                                        for that we need to write before pip3 install flask

RUN pip3 install flask: 
                         install flask

WORKDIR /app:
             /app directory of work

COPY ./api.py /app/api.py:
                         copy file api.py to /app/api.py in container

CMD [ "python3", "api.py" ]:
                           method for runnig app flask

