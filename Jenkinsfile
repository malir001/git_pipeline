pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                cleanWs()
                echo 'Building a new laptop'
                sh 'mkdir build'
                sh 'touch build/computer.txt'
                sh 'echo "Mainboard" >> build/computer.txt'
                sh 'cat build/computer.txt'
                sh 'echo "computer" >> build/computer.txt'
                sh 'cat build/computer.txt'
                sh 'echo "keyboard" >> build/computer.txt'
                sh 'cat build/computer.txt'
            }
        }
        stage ('Test'){
            steps{
                echo 'Testing the new laptop...'
            }
        }
        
        
    }
    
    
    }
