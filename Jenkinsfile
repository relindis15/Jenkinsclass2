pipeline {
    agent any
    tools {
        maven 'local maven'
    }
    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/relindis15/Jenkinsclass2.git',
                    credentialsId: 'jay',
                    branch 'main'
            }
        }
    }
}


