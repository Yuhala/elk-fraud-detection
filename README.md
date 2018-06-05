# ELK-simbox-fraud-detection
A simbox-fraud detection tool based on the ELK stack.

## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See [documentation](documentation-simbox-fraud-detection.pdf) for more information on the project.

### Prerequisites

To follow this tutorial with minimal hiccups you need Ubuntu 16.04 server and a non-root user with sudo priviledges. 

## Installing Docker and Docker Compose
The following commands will install docker and docker compose on your linux machine.

### Installing Docker
First, add the GPG key for the official Docker repository to the system:

```
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

```
Add the Docker repository to APT sources:

```
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"

```
Update the package database with the Docker packages from the newly added repo:

```
sudo apt-get update

```
Install Docker

```
sudo apt-get install -y docker-ce

```
### Installing Docker Compose
Check the current release and if necessary, update it in the command below; version 1.18.0 was used for this project

```
sudo curl -L https://github.com/docker/compose/releases/download/1.18.0/docker-compose-`uname -s`-`uname -m` -o /usr/local/bin/docker-compose

```
Set the permissions:

```
sudo chmod +x /usr/local/bin/docker-compose

```
Verify that the installation was successful by checking the version:

```
docker-compose --version

```

## Obtaining the main project folder from google drive

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
Running the images: cd into `elkdocker/docker-compose` and open your terminal. Type the following command to run the images

```
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

All steps required for deploying and using this application can be found in `Chapter 3` of the [documentation](documentation-simbox-fraud-detection.pdf) file.

## Built With

* [ELK Stack](https://www.elastic.co/webinars/introduction-elk-stack) - A powerful open-source log management platform


## Authors

* **Peterson Yuhala** 

See also the list of [contributors](https://github.com/your/project/contributors) who participated in this project.

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details

## Acknowledgments

* Tim Roes - [Kibana Tutorials](https://www.timroes.de/2015/02/07/kibana-4-tutorial-part-1-introduction/)
