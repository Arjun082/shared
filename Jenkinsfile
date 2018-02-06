@Library("github.com/Arjun082/shared@master")_
    def defaultconfigtxt = libraryResource 'spring/test'
    def defaultconfig = readProperties text: defaultconfigtxt
    echo "${defaultconfig.ENV}"
node {
    stage('Checkout') {
        git(
           url: "${defaultconfig.GIT_URL}",
           branch: "${defaultconfig.BRANCH}"
        )
    }
    
}
