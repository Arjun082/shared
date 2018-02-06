pipeline {
    def config = [:]
    agent any
    tools {
    maven 'maven'
  }
    def defaultconfigtxt =libraryResource 'spring/DefaultConfiguration'
    def defaultconfig = readProperties text: defaultconfigtxt
    echo '${defaultconfig}'
    stages {
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
}
