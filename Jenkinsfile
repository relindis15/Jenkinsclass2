pipeline {
    agent any
    tools {
        maven "local maven"
    }
    environment {

    PATH = "C:\\WINDOWS\\SYSTEM32"

}

    stages {
        stage('Checkout') {
            steps {
                // Get some code from a GitHub repository
                git url: 'https://github.com/relindis15/Jenkinsclass2.git', 
                    branch: 'main',
                    credentialsId: 'jay'
            }
        
        }
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package' 
            }
        
        }
        stage('Test'){
            steps {
                bat 'mvn test'
            }
            post {
             always {
                  junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}



