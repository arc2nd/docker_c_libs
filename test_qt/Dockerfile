FROM library_qt:latest

RUN apt-get install -y vim

COPY . /srv/app
WORKDIR /srv/app

CMD ["python", "/srv/app/py_wait.py"] 
