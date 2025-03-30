pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                print "checkout"
                checkout([
                    $class: 'GitSCM'
                branches: [['*/main']]
                useRemoteConigs: [ [
                    credentialsId: 'ThophopPhe',
                    url: 'https://github.com/thiphop/403.git'
                ]]
                ])
                print "checkoutSuc"
            }
        }
    }
}