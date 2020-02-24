pipeline {
    agent any
    tools 
    { 
        maven 'maven' 
    }
    stages
    
    {
        stage ('Init stage') 
        {
            steps 
            {
                git credentialsId: 'f017161e-31e0-45df-bafe-9afa4c3903ef', url: 'https://github.com/venkatarajv/mavenproject.git'
            }
        }
        stage ('compile stage') 
        {
            steps 
            {
                sh "mvn clean install"
                sh "mvn clean package"
                sh "mvn clean compile"
            }
        }
        stage ('Test Stage') 
        {
            steps 
            {
                sh 'mvn test'
                
            }
        }
        stage ('Deployment Stage') 
        {
            steps 
            {
                sh 'mvn install'
                sh 'mvn tomcat:deploy '
                
            }
        }
    }
}
