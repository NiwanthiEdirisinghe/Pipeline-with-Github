pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project'
                writeFile file: 'buildLog.txt', text: 'Build log content here.'
            }
            post {
                always {
                    mail to: 'niwanthiedirisinghe.95@gmail.com',
                         subject: "Build Stage Status: ${currentBuild.currentResult}",
                         body: "The Build stage has completed with status: ${currentBuild.currentResult}.",
                         attachLog: true,                
                        attachmentsPattern: 'buildLog.txt'
                }
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests'
                writeFile file: 'testResults.txt', text: 'Test results here.'
            }
            post {
                always {
                    mail to: 'niwanthiedirisinghe.95@gmail.com',
                         subject: "Unit and Integration Tests Status: ${currentBuild.currentResult}",
                         body: "The Unit and Integration Tests stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analyzing code'
                writeFile file: 'codeAnalysis.txt', text: 'Code analysis results here.'
            }
            post {
                always {
                    mail to: 'niwanthiedirisinghe.95@gmail.com',
                         subject: "Code Analysis Status: ${currentBuild.currentResult}",
                         body: "The Code Analysis stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing Security Scan'
                writeFile file: 'securityScan.txt', text: 'Security scan results here.'
            }
            post {
                always {
                    mail to: 'niwanthiedirisinghe.95@gmail.com',
                         subject: "Security Scan Status: ${currentBuild.currentResult}",
                         body: "The Security Scan stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging'
                writeFile file: 'stagingDeployment.txt', text: 'Staging deployment log here.'
            }
            post {
                always {
                    mail to: 'niwanthiedirisinghe.95@gmail.com',
                         subject: "Deploy to Staging Status: ${currentBuild.currentResult}",
                         body: "The Deploy to Staging stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Integration Tests on Staging'
                writeFile file: 'stagingTests.txt', text: 'Staging integration tests results here.'
            }
            post {
                always {
                    mail to: 'niwanthiedirisinghe.95@gmail.com',
                         subject: "Integration Tests on Staging Status: ${currentBuild.currentResult}",
                         body: "The Integration Tests on Staging stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production'
                writeFile file: 'productionDeployment.txt', text: 'Production deployment log here.'
            }
            post {
                always {
                    mail to: 'niwanthiedirisinghe.95@gmail.com',
                         subject: "Deploy to Production Status: ${currentBuild.currentResult}",
                         body: "The Deploy to Production stage has completed with status: ${currentBuild.currentResult}."
                }
            }
        }
    }
}
