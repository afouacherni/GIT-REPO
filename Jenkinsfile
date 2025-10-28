pipeline {
    agent any
    tools {
        jdk 'JDK-17'
    }
    stages {
        stage('Checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/afouacherni/GIT-REPO.git'
            }
        }
        stage('Compile code') {
            steps {
                sh 'javac Test.java'
            }
        }
        stage('Execute code') {
            steps {
                sh 'java Test'
            }
        }
    }
}
