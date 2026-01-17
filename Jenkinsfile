pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building app'
            }
        }

        stage('Docker Build') {
            steps {
                sh 'docker build -t jenkins-demo:v1 .'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                docker rm -f jenkins-app || true
                docker run -d -p 8081:80 --name jenkins-app jenkins-demo:v1
                '''
            }
        }
    }
}

