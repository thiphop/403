pipeline {
    agent any
    stages {
        stage('checkout') {
            steps {
                script {
                    echo "checkout"
                    checkout([
                        $class: 'GitSCM',
                        branches: [[name: '*/main']],
                        userRemoteConfigs: [[
                            credentialsId: 'ThiphopPhe',
                            url: 'https://github.com/thiphop/403.git'
                        ]]
                    ])
                    echo "checkoutSuc"
                }
            }
        }
    }
}