pipeline {
    agent {
        docker { image 'maven:3-alpine' }
    }
    stages {
        stage('checkout') {
            steps {
                git 'https://github.com/AdamClifford94/maven_test.git'
            }
        }
        stage('test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('clean & package') {
            steps {
                sh 'mvn clean'
                sh 'mvn package'
            }
        }
        stage('install') {
            steps {
                sh 'mvn install'
            }
        }
    }
}
