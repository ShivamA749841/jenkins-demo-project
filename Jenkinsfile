pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Getting Java project from GitHub...'
            }
        }

        stage('Build') {
            steps {
                bat 'javac Calculator.java'
            }
        }

        stage('Test') {
            steps {
                echo 'Testing Calculator...'
            }
        }

        stage('Run') {
            steps {
                bat 'java Calculator'
            }
        }
    }

    post {
        success {
            echo 'Calculator pipeline completed successfully!'
        }

        failure {
            echo 'Calculator pipeline failed!'
        }
    }
}
