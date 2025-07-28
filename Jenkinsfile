pipeline {
    agent any
    tools {
        maven 'maven3.6'
        jdk 'jdk17'
    }
    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Mousaabca89/BoardGame.git'
            }
        }
        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }        
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }        
        stage('Package') {
            steps {
                sh 'mvn package'
            }
        }
        stage('Hello') {
            steps {
                echo 'Webhook trigger'
            }
        }
    }
}
