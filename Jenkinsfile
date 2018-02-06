#!/usr/bin/env groovy
    def config = [:]
node() {
   //def defaultconfigtxt = libraryResource '/spring/DefaultConfiguration'
    def defaultconfig = readProperties file: 'resources/spring/DefaultConfiguration'
    echo "${defaultconfig}"
    stage('Back-end') {
                git url: "https://github.com/safirh/petclinic.git"
        }
        stage('maven') {
                sh 'mvn clean install -DskipTests=true'
        }  
}   
