pipeline {
    agent { docker 'node:6.3' }
    stages {
        stage('build') {
            steps {
                sh 'npm --version'
                sh 'node --version'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
    }
}
