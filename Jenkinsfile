pipeline {
    agent any

    stages {
        stage('Clean') {
            steps {
                echo 'Cleaning workspace...'
                deleteDir()
            }
        }

        stage('Checkout') {
            steps {
                git 'https://github.com/Yashdeep22/jenkins-ci-pipeline-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Compiling Java file...'
                sh 'javac Test.java'
            }
        }

        stage('Run') {
            steps {
                echo 'Running Java program...'
                sh 'java Test'
            }
        }
    }
}
