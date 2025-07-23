pipeline {
    agent any

    stages {
        stage('Build') {
            agent{
                    docker{
                        image 'node:18-alpine'
                        reuseNode true
                    }
                }
            steps {
                               
                sh '''
                ls -la
                node --version
                npm --version
                
                sh 'rm -rf node_modules dist' 
                sh 'npm ci'
                sh 'npm run build'
                ls -la
                '''
               

                   }
        }
        stage ('Test'){
            steps{
                echo 'Testing the new laptop...'
            }
        }
        
        
    }
    
    
    }
