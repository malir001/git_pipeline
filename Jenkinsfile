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
                
                npm run build
                npm install
                npm start
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
