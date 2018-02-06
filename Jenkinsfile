Library("github.com/Arjun082/shared@master")_

node {
    stage('read properties') {
        def defaultconfigtxt = libraryResource 'spring/test'
        def defaultconfig = readProperties text: defaultconfigtxt
        echo "${defaultconfig.ENV}"
    }
    stage('Checkout') {
        git(
           url: "${defaultconfig.GIT_URL}",
           branch: "${defaultconfig.MASTER}"
        )
    }
    
} 
