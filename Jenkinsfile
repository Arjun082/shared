#!/usr/bin/env groovy
def config = [:]
node() {
   def defaultconfigtxt = libraryResource '/spring/DefaultConfiguration'
   def defaultconfig = readProperties text: 'defaultconfigtxt'
    echo "${defaultconfig}"
    stage('Back-end') {
                git url: "https://github.com/safirh/petclinic.git"
                echo "${config.GIT_URL}"
        }
}   
