pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'make'
            }
        }
        stage('Test') { 
            steps {
               sh 'make check'
              xunit 'report/**/*.xml'
            }
        }
        stage('Deploy') { 
            steps {
                sh 'make publish'
            }
        }
    }
}
