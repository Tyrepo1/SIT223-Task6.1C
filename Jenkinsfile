pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the code using Maven...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests using Jest...'
                echo 'Running integration tests using Selenium'
                emailext subject: "Test notification",
                          body: "Test is a Success",
                          to: 'dimonkey1912@gmail.com',
                          attachLog: true
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Running code analysis with SonarQube...'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing security scan with SonarQube...'
                emailext subject: "Security notification",
                          body: "Security is a Success",
                          to: 'dimonkey1912@gmail.com',
                          attachLog: true
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying the application to staging server (AWS EC2 instance)...'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running integration tests on staging environment using Selenium...'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying the application to production server (AWS EC2 instance)...'
            }
        }
    }
}
