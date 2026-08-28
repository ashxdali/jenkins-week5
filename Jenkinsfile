pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage started'
                sh 'chmod +x app.sh'
                sh './app.sh'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                sh 'test -f wrongfile.sh'
            }
        }

        stage('Validation') {
            steps {
                echo 'Validation successful'
                sh 'bash -n app.sh'
            }
        }
    }
}
