pipeline {
    agent any

    tools {
        maven 'Maven3'
    }

    options {
        skipDefaultCheckout(true)
    }

    stages {

        stage('CHECKOUT') {
            steps {
                git branch: 'main', url: 'https://github.com/knVeerendra/Demo.git'
            }
        }

        stage('Build') {
            steps {
                dir('demo') {
                    bat 'mvn clean install -Dmaven.compiler.source=8 -Dmaven.compiler.target=8'
                }
            }
        }

        stage('Test') {
            steps {
                dir('demo') {
                    bat 'mvn test -Dmaven.compiler.source=8 -Dmaven.compiler.target=8'
                }
            }
        }
    }
}
