#!/usr/bin/env groovy
ansicolor('xterm')
def config = [:]
//def defaultconfigtxt = libraryResource '/spring/DefaultConfiguration'

node() {
    stage('Back-end') {
        checkout scm
        def defaultconfig = readProperties file: "resources/spring/DefaultConfiguration"
        echo "${defaultconfig}"
        config = readproperties defaults: defaultconfig, file: "'resources/spring/test"
        git url: "https://github.com/safirh/petclinic.git"
        echo "${config.ENV}"
        }
}   
