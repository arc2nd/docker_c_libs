This repo is a place to store examples of building docker containers that have specific 
C++ libraries installed. The purpose is to be able to compile c++ programs in a contained 
environment without polluting the host computer with too many dependencies.

Steps to use:

* Each library gets build into a docker image with no cmd called "library_<library_name>"
* Then I build an image from that library image that runs "py_wait.py" called "my_<library_name>"
* Then I instance that image into a container called "<library_name>_compiler"
* Then I 'docker exec /bin/bash' into that container to run the compile

Technoligies that I know I want to include:
* Qt5
* openCV
* JSON
* AMQP
* MQTT
* REST
