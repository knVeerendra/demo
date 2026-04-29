pipeline {
    agent any

    tools {
        maven 'Maven3'
    }

    stages {

        stage('CHECKOUT') {
            steps {
                git branch: 'main', url: 'https://github.com/knVeerendra/Demo.git'
            }
        }

        stage('BUILD') {
            steps {
                dir('demo') {
                    bat 'mvn clean install'
                }
            }
        }

        stage('TEST') {
            steps {
                dir('demo') {
                    bat 'mvn test'
                }
            }
        }
    }
}