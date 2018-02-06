#!/usr/bin/env groovy
def config = [:]
node() {
    stage('Back-end') {
        def defaultconfigtxt = libraryResource 'spring/DefaultConfiguration'
        def defaultconfig = readProperties text: defaultconfigtxt
        config = readproperties defaults: defaultconfig, file: "resources/spring/test"
        git url: "https://github.com/safirh/petclinic.git"
        echo "${config.ENV}"
        }
}   
