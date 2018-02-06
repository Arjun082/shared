#!/usr/bin/env groovy
def config = [:]
node() {
    stage('Back-end') {
        checkout scm
       // def defaultconfigtxt = libraryResource '/spring/DefaultConfiguration'
        def defaultconfig = readProperties file: "resources/spring/DefaultConfiguration"
        config = readproperties defaults: defaultconfig, file: "resources/spring/test"
        git url: "https://github.com/safirh/petclinic.git"
        echo "${config.ENV}"
        }
}   
