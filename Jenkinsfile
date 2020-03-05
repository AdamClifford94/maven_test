pipeline {
    agent {
        docker { image 'maven:3-alpine' }
    }
    stages {
        stage('SCM Checkout') {
            steps {
                git 'https://github.com/AdamClifford94/maven_test.git'
            }
        }
        stage('Test-Package') {
            steps {
                sh 'mvn test'
            }
        }
        stage('Compile-Package') {
            steps {
                sh 'mvn clean'
                sh 'mvn package'
            }
        }
        stage('install-Package') {
            steps {
                sh 'mvn install'
            }
        }        
    }
}
