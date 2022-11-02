pipeline {
    agent any
    tools {
        maven "local maven"
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
    }
}
stage('Build') {
    steps {
        bat 'mvn -B -DskipTests clean package' 
    }
}


