pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')
    }

    stages {

        stage('Build') {
            steps {
                echo 'Task: Compile and package the application'
                echo 'Tool: Maven'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit and integration tests'
                echo 'Tools: JUnit and Postman/Newman'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse source code quality'
                echo 'Tool: SonarQube'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Scan application for security vulnerabilities'
                echo 'Tool: OWASP Dependency-Check'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy application to staging environment'
                echo 'Tool: AWS EC2 / AWS CLI'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests in staging environment'
                echo 'Tool: Postman/Newman'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy application to production environment'
                echo 'Tool: AWS EC2 / AWS CLI'
            }
        }
    }
}
 
