pipeline { 
    agent any 
 
    tools { 
        
        maven 'Maven3' 
    } 
 
    stages {
        stage('CHECKOUT') { 
            steps { 
                git 'your_github_repo_link' 
            } 
        } 
 
        stage('Build') { 
            steps { 
                dir('demo'){ 
                bat 'mvn clean install' 
            } 
            } 
        } 
        stage('Test') { 
            steps { 
                dir('demo'){ 
                bat 'mvn test' 
            } 
            } 
        } 
    }    
}
