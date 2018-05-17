# ELK-simbox-fraud-detection
A simbox-fraud detection tool based on the ELK stack.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See [documentation](documentation.pdf) for more information on the project.

### Prerequisites

To follow this tutorial with minimal hiccups you need Ubuntu 16.04 server and a non-root user with sudo priviledges. 

### Installing docker and docker compose
The following commands will install docker and docker compose on your linux machine.

```
#Installing docker
sudo apt-get update
sudo apt-get install curl
curl -ssl https://get.docker.com | sh

#Installing docker compose
sudo curl -L https://github.com/docker/compose/releases/download/1.18.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
```

### Obtaining the main project folder from google drive

The main project folder can be found on google drive using the below link:

```
https://drive.google.com/file/d/1vyJL5DpNj-cghS1GvJlJyDlzhBTVlDH1/edit
```
Unzip the zip file downloaded

## Installing and Running the docker images
Here we will pull all the docker images from docker hub and run them on our local machine.

Run docker service
```
sudo service docker start
```
Pulling the images from docker hub
```
docker pull pyuhala01/cdr_gen
docker pull pyuhala01/elasticsearch
docker pull pyuhala01/logstash
docker pull pyuhala01/kibana

```
Running the images: cd into elkdocker/docker-compose and open your terminal
```
#Run the docker images
sudo docker-compose up
```

### Tests

To test if the elasticsearch service is up and running, enter the below link in your browser.

```
http://localhost:9200
```
The elasticsearch JSON interface should appear.

To test if the kibana service is up and running, enter the below link in your browser.

```
http://localhost:5601
```
The kibana interface should appear in your browser.


## How to use the program

All steps required for deploying and using this application can be found in Chapter 3 of the [documentation](documentation.pdf) file.

## Built With

* [ELK Stack](http://www.dropwizard.io/1.0.2/docs/) - A powerful open-source log management platform


## Authors

* **Peterson Yuhala** - *Initial work* - [PurpleBooth](https://github.com/PurpleBooth)

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details

## Acknowledgments

* Tim Roes - [Kibana Tutorials](https://www.timroes.de/2015/02/07/kibana-4-tutorial-part-1-introduction/)
