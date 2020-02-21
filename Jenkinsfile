pipeline {
    agent any
    tools { 
        maven 'Maven 3.1' 
        jdk '1.8.0_222-ea' 
    }
    stages {
        stage ('Initialize') {
            steps {
                sh '''
                    echo "PATH = ${PATH}"
                    echo "M2_HOME = ${M2_HOME}"
                    mvn clean compile
                ''' 
            }
        }
        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }
        stage ('Build') {
            steps {
                echo 'This is a minimal pipeline.'
            }
        }
    }
}