/* groovylint-disable-next-line CompileStatic */
pipeline {
    agent { docker { image 'node:20.17.0-alpine3.20' } }
    stages {
        stage('build') {
            steps {
                // sh 'docker -v'
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

    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
