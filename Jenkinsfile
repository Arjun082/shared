#!/usr/bin/env groovy
    def config = [:]
node() {
   //def defaultconfigtxt = libraryResource '/spring/DefaultConfiguration'
    def defaultconfig = readProperties file: 'resources/spring/DefaultConfiguration'
    echo '${defaultconfig}'
    stage('Back-end') {
            steps {
                git '${config.GIT_URL}'
            }
        }
        stage('maven') {
            steps {
                sh 'mvn clean install -DskipTests=true'
                
            }
        }  
}   
