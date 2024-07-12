pipeline {
    agent any
    
    tools{
    jdk 'jdk17'
    maven  'maven'
}

    stages {
        
        
        stage('Git Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/helalcse2k/Petclinic.git'
            }
        }
        
        
        stage('Compile') {
            steps {
                sh "mvn clean compile"
            }
        }
        
        
        
        stage('Build') {
            steps {
                sh "mvn clean package"
            }
        }
        
        
        stage('Deploy') {
            steps {
                sh "sudo cp target/petclinic.war /opt/apache-tomcat-9.0.67/webapps" 
            }
        }
        
        
    }
}
