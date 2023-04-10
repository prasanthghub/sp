pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/prasanthghub/springboot.git'
            }
        }
        
        stage('Compile (slave-1)') {
            agent {
                node {
                    label 'node1'
                }
            }
            steps {
                sh 'mvn clean compile '
            }
        }
        
        stage('Compile (slave-2)') {
            agent {
                node {
                    label 'node2'
                }
            }
            steps {
                sh 'mvn clean compile '
            }
        }
        
        
    }
}
