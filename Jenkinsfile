pipeline {
    agent any
    stages {
        stage('clean') {
            steps {
                bat 'mvn clean'
            }
        }
        stage('compile') {
            steps {
                bat 'mvn compile'
            }
        }
        stage('test') {
            steps {
                bat 'mvn test'
            }
        }
        stage('Deploy') {
            when {
              expression {
                currentBuild.result == null || currentBuild.result == 'SUCCESS' 
              }
            }
            steps {
                bat 'make publish'
            }
        }
    }
     post {
        always {
            mail to: 'karthick.inform@gmail.com'
            subject: 'test'
            body: 'test1'
        }
    }
}
