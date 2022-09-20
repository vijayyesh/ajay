#!/bin/bash
sudo apt update
sudo apt install openjdk-11-jdk -y
wget https://dlcdn.apache.org/solr/solr/9.0.0/solr-9.0.0.tgz
tar xzf solr-9.0.0.tgz solr-9.0.0/bin/install_solr_service.sh --strip-components=2
sudo apt-get update
sudo bash ./install_solr_service.sh solr-9.0.0.tgz
sudo service solr start
