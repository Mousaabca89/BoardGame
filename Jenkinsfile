pipeline {
    agent any    
    tools {
        maven 'maven3.9'
        jdk 'jdk17'
    }
    parameters {
        string(name: 'Branch_name', defaultValue: 'main', description: 'Git Branch to Build')
    }
    stages {
        stage('Git Checkout') {
            steps {
                git branch: "$(params.Branch_name)", url: 'https://github.com/Mousaabca89/BoardGame.git'
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
    }
}
