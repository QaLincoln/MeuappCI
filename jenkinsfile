pipeline {
    agent any
     tools {
        nodejs "node 22.11.0"
     }

     stages {
        stage('Checkout') {
            steps {
                Checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/QaLincoln/MeuappCI.git']]])
            }
        }

        stage('Build') {
            steps {
                bat 'npm install'
                bat 'npm run build'
            }
        }

        stage('Run Unit Tests') {
            steps {
                bat 'npm run test'
            }
        }
        
     }
}