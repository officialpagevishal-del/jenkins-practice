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
    }
}

