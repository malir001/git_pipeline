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
                
                rm -rf node_modules dist
                npm ci
                npm run build
                ls -la
                '''
               

                   }
        }
        stage ('Test'){
            steps{
                sh 'test -f build/index.html'
            }
        }
        
        
    }
    
    
    }
