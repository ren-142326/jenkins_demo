pipeline {
    agent { docker { image 'node:20.17.0-alpine3.20' } }
    stages {
        stage('build') {
            steps {
                sh 'docker -v'
                sh 'node -v'
                sh 'npm -v'
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}
