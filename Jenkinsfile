pipeline {
    agent any
    stages {
        stage('Compile and Test on Node 1') {
            agent { label 'node1' }
            steps {
                sh 'mvn clean compile test'
            }
        }
        stage('Compile and Test on Node 2') {
            agent { label 'node2' }
            steps {
                sh 'mvn clean compile test'
            }
        }
    }
}
