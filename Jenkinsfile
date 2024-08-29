pipeline {
    agent any

    environment {
        EMAIL_RECIPIENT = 'niwanthiedirisinghe.95@gmail.com'
    }

    stages {
        stage('Build') {
            steps {
                script {
                    echo 'Task: Build the code using a build automation tool updated.'
                    echo 'Tool: Maven'
                }
            }
            post {
                success {
                    emailext(
                        to: "${EMAIL_RECIPIENT}",
                        subject: "Build Stage Success: ${currentBuild.currentResult}",
                        body: "The Build stage has completed successfully.",
                    )
                }
            }
        }
        
        stage('Unit and Integration Tests') {
            steps {
                script {
                    echo 'Task: Run unit tests to ensure code functions as expected and integration tests.'
                    echo 'Tool: JUnit'
                }
            }
            post {
                success {
                    emailext(
                        to: "${EMAIL_RECIPIENT}",
                        subject: "Unit and Integration Tests Success: ${currentBuild.currentResult}",
                        body: "The Unit and Integration Tests stage has completed successfully.",
                    )
                }
            }
        }
        
        stage('Code Analysis') {
            steps {
                script {
                    echo 'Task: Analyze the code to ensure it meets industry standards.'
                    echo 'Tool: SonarQube'
                }
            }
            post {
                success {
                    emailext(
                        to: "${EMAIL_RECIPIENT}",
                        subject: "Code Analysis Success: ${currentBuild.currentResult}",
                        body: "The Code Analysis stage has completed successfully.",
                    )
                }
            }
        }
        
        stage('Security Scan') {
            steps {
                script {
                    echo 'Task: Perform a security scan on the code to identify vulnerabilities.'
                    echo 'Tool: OWASP Dependency-Check'
                }
            }
            post {
                success {
                    emailext(
                        to: "${EMAIL_RECIPIENT}",
                        subject: "Security Scan Success: ${currentBuild.currentResult}",
                        body: "The Security Scan stage has completed successfully.",
                    )
                }
            }
        }
        
        stage('Deploy to Staging') {
            steps {
                script {
                    echo 'Task: Deploy the application to a staging server.'
                    echo 'Tool: Custom deployment script'
                }
            }
            post {
                success {
                    emailext(
                        to: "${EMAIL_RECIPIENT}",
                        subject: "Deploy to Staging Success: ${currentBuild.currentResult}",
                        body: "The Deploy to Staging stage has completed successfully.",
                    )
                }
            }
        }
        
        stage('Integration Tests on Staging') {
            steps {
                script {
                    echo 'Task: Run integration tests on the staging environment to ensure functionality.'
                    echo 'Tool: Maven or similar'
                }
            }
            post {
                success {
                    emailext(
                        to: "${EMAIL_RECIPIENT}",
                        subject: "Integration Tests on Staging Success: ${currentBuild.currentResult}",
                        body: "The Integration Tests on Staging stage has completed successfully.",
                    )
                }
            }
        }
        
        stage('Deploy to Production') {
            steps {
                script {
                    echo 'Task: Deploy the application to a production server.'
                    echo 'Tool: Custom deployment script'
                }
            }
            post {
                success {
                    emailext(
                        to: "${EMAIL_RECIPIENT}",
                        subject: "Deploy to Production Success: ${currentBuild.currentResult}",
                        body: "The Deploy to Production stage has completed successfully.",
                    )
                }
            }
        }
    }
}
