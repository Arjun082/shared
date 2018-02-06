#!/usr/bin/env groovy
def config = [:]
def defaultconfigtxt = libraryResource "/spring/DefaultConfiguration"
def defaultconfig = readProperties text: "defaultconfigtxt"
node() {
    stage('Back-end') {
        checkout scm
        config = readproperties defaults: defaultconfig, file: "'resources/spring/test"
        git url: "https://github.com/safirh/petclinic.git"
        echo "${config.ENV}"
        }
}   
