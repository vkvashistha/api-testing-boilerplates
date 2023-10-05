pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        
        stage('Install Dependencies') {
            steps {
                sh 'npm install -g newman'
            }
        }
        
        stage('Run Postman Tests') {
            steps {
                sh 'newman run demo.postman_collection.json'
            }
        }
    }
}
