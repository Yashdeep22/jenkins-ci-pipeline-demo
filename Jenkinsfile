pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
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
}
