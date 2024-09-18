pipeline {
    agent { docker 'node:20.17' }
    stages {
        stage('build') {
            steps {
                sh 'echo "Hello World"'
                sh 'npm --version'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}
