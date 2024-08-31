pipeline {
    agent any
    
    environment {
        GIT_REPO_URL = 'https://github.com/ranjithk9/lmbda.git'
         BRANCH = 'main'
        GIT_TOOL = 'DefaultGit'  // Replace 'DefaultGit' with the name of your configured Git tool
        MAVEN_HOME = 'path/to/maven'
    }
     tools {
        git "${GIT_TOOL}"
    }
      
    stages {
        stage('Checkout') {
            steps {
                // Clone the repository
                git branch: 'main', credentialsId: '49951596-8e02-4d93-b7bb-c5371320b7f5', url: 'https://github.com/ranjithk9/lmbda.git'}
        }
        stage('Compile') {
            steps {
                // Clean and compile the project using Maven
                sh "${MAVEN_HOME}/bin/mvn clean compile install"
            }
        }

          stage('Test') {
            steps {
                // Run unit tests
                sh "${MAVEN_HOME}/bin/mvn test"
            }
            }    
    
    }
         
}  

            
            
            
            
            
            
            
            
            
            
            
    
        
      
        
                
       
        
    

