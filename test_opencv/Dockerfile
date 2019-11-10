FROM library_opencv:latest

RUN apt-get -y install vim

COPY . /srv/app
WORKDIR /srv/app

CMD ["python", "/srv/app/py_wait.py"] 
