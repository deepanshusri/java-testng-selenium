pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the source code from your version control system
                // For example, using Git
                git 'https://github.com/deepanshusri/java-testng-selenium.git'
            }
        }
        
        stage('Build') {
            steps {
                // Build your Java project
                // For example, using Apache Maven
                sh 'mvn clean package'
                sh 'mvn install'
            }
        }
        
        stage('Test') {
            steps {
                // Run tests for your Java project
                // For example, using Apache Maven
               // bat 'mvn test'
                sh 'mvn test -D suite=single.xml'
            }
        }
        
        stage('Deploy') {
            steps {
                // Deploy your Java project to a server or a container
                // For example, using Docker
                sh 'docker build -t your-image .'
                sh 'docker run -d -p 8080:8080 your-image'
            }
        }
    }
}
