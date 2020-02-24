pipeline {
    agent any
    tools { 
        maven 'maven' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    mvn clean compile
                ''' 
            }
        }
        stage ('Testing Stage') {

            steps {
               
                    sh 'mvn test'
            }
        }
        stage ('Build') {
            steps {
                echo 'This is a minimal pipeline.'
            }
        }
    }
}