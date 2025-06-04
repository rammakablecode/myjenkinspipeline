pipeline {
    agent any
    triggers {
        pollSCM('H/1 * * * *') // Triggers every 15 minutes
    }
    stages {
        stage('Build') {
            steps {
                echo 'Stage 1: Build - Using Maven to compile and package code.'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Stage 2: Testing - Running JUnit for unit tests and TestNG for integration tests.'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Stage 3: Code Analysis - Using SonarQube to analyze code quality and standards.'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Stage 4: Security Scan - Using OWASP Dependency-Check to scan for vulnerabilities.'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Stage 5: Deploy to Staging - Deploying to AWS EC2 using Ansible.'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Stage 6: Staging Tests - Running Postman or Newman tests against staging environment.'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Stage 7: Deploy to Production - Deploying final version to production AWS EC2 using Ansible.'
            }
        }
    }
}
