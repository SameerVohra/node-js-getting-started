pipeline {
    agent any
    
    environment {
        NODE_HOME = tool 'NodeJS'
        PATH = "${NODE_HOME}\\bin;${env.PATH}" // Windows uses backslashes (`\`)
    }
    
    stages {
        stage('Install Dependencies') {
            steps {
                bat 'npm install'
            }
        }
        
        stage('Build') {
            steps {
                bat 'npm run build'
            }
        }
        
        stage('Test') {
            steps {
                bat 'npm test'
            }
        }
        
        stage('Deploy') {
            steps {
                bat 'npm start'
            }
        }
    }
}
