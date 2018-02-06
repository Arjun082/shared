#!/usr/bin/env groovy
def config = [:]
def defaultconfigtxt = libraryResource '/spring/DefaultConfiguration'
def defaultconfig = readProperties text: 'defaultconfigtxt'
echo "${defaultconfig}"
node() {
    stage('Back-end') {
                git url: "https://github.com/safirh/petclinic.git"
                echo "${config.GIT_URL}"
        }
}   
