pipeline {
    agent any

    environment {
        JAVA_HOME = "${tool 'jdk21'}"
        PATH = "${env.JAVA_HOME}\\bin;${env.PATH}"
    }

    stages {
        stage('Clean') {
            steps {
                echo 'Cleaning workspace...'
                deleteDir()
            }
        }

        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                git 'https://github.com/Yashdeep22/jenkins-ci-pipeline-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java file...'
                bat 'javac Test.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Java program...'
                bat 'java Test'
            }
        }
    }

    post {
        success {
            echo '✅ Build and execution successful!'
        }
        failure {
            echo '❌ Build or execution failed.'
        }
        always {
            echo 'Pipeline finished.'
        }
    }
}
