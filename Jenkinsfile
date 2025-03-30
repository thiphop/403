pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                script {
                    print "checkout"
                    checkout([
                        $class: 'GitSCM',
                        branches: [[name: '*/main']],
                        userRemoteConfigs: [[
                            credentialsId: 'ThiphopPhe',
                            url: 'https://github.com/thiphop/403.git'
                        ]]
                    ])
                    print "checkoutSuccess"
                }
            }
        }

        stage('testRobot') {
            steps {
                sh 'pip install robotframework'
                print "install Success"
            }
        }
    }
}