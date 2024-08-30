FROM python:3.9-slim

WORKDIR /app

COPY requirement.txt requirement.txt
#we have in requirement.txt flask and flask-cors

RUN pip install -r requirement.txt

COPY . .
# copy all file from directory to container

EXPOSE 5252
# port of execute

CMD [ "python3", "api.py" ]
