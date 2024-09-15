pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Task: Build the code using a build automation tool updated.'
                echo 'Tool: Maven'
                writeFile file: 'buildLog.txt', text: 'Build log content here.'
            }
            post {
                always {
                    archiveArtifacts artifacts: 'buildLog.txt', onlyIfSuccessful: true
                    emailext(
                        to: 'niwanthiedirisinghe.95@gmail.com',
                        subject: "Build Stage Status: ${currentBuild.currentResult}",
                        body: "The Build stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true,
                        attachmentsPattern: 'buildLog.txt'
                    )
                }
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests and integration tests.'
                echo 'Tool: JUnit'
                writeFile file: 'testResults.txt', text: 'Test results here.'
            }
            post {
                always {
                    archiveArtifacts artifacts: 'testResults.txt', onlyIfSuccessful: true
                    emailext(
                        to: 'niwanthiedirisinghe.95@gmail.com',
                        subject: "Unit and Integration Tests Status: ${currentBuild.currentResult}",
                        body: "The Unit and Integration Tests stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true,
                        attachmentsPattern: 'testResults.txt'
                    )
                }
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Task: Analyze the code to ensure it meets industry standards.'
                echo 'Tool: SonarQube'
                writeFile file: 'codeAnalysis.txt', text: 'Code analysis results here.'
            }
            post {
                always {
                    archiveArtifacts artifacts: 'codeAnalysis.txt', onlyIfSuccessful: true
                    emailext(
                        to: 'niwanthiedirisinghe.95@gmail.com',
                        subject: "Code Analysis Status: ${currentBuild.currentResult}",
                        body: "The Code Analysis stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true,
                        attachmentsPattern: 'codeAnalysis.txt'
                    )
                }
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Task: Perform a security scan on the code.'
                echo 'Tool: OWASP Dependency-Check'
                writeFile file: 'securityScan.txt', text: 'Security scan results here.'
            }
            post {
                always {
                    archiveArtifacts artifacts: 'securityScan.txt', onlyIfSuccessful: true
                    emailext(
                        to: 'niwanthiedirisinghe.95@gmail.com',
                        subject: "Security Scan Status: ${currentBuild.currentResult}",
                        body: "The Security Scan stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true,
                        attachmentsPattern: 'securityScan.txt'
                    )
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to a staging server.'
                echo 'Tool: Custom deployment script'
                writeFile file: 'stagingDeployment.txt', text: 'Staging deployment log here.'
            }
            post {
                always {
                    archiveArtifacts artifacts: 'stagingDeployment.txt', onlyIfSuccessful: true
                    emailext(
                        to: 'niwanthiedirisinghe.95@gmail.com',
                        subject: "Deploy to Staging Status: ${currentBuild.currentResult}",
                        body: "The Deploy to Staging stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true,
                        attachmentsPattern: 'stagingDeployment.txt'
                    )
                }
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests on the staging environment.'
                echo 'Tool: Maven'
                writeFile file: 'stagingTests.txt', text: 'Staging integration tests results here.'
            }
            post {
                always {
                    archiveArtifacts artifacts: 'stagingTests.txt', onlyIfSuccessful: true
                    emailext(
                        to: 'niwanthiedirisinghe.95@gmail.com',
                        subject: "Integration Tests on Staging Status: ${currentBuild.currentResult}",
                        body: "The Integration Tests on Staging stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true,
                        attachmentsPattern: 'stagingTests.txt'
                    )
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the application to a production server.'
                echo 'Tool: Custom deployment script'
                writeFile file: 'productionDeployment.txt', text: 'Production deployment log here.'
            }
            post {
                always {
                    archiveArtifacts artifacts: 'productionDeployment.txt', onlyIfSuccessful: true
                    emailext(
                        to: 'niwanthiedirisinghe.95@gmail.com',
                        subject: "Deploy to Production Status: ${currentBuild.currentResult}",
                        body: "The Deploy to Production stage has completed with status: ${currentBuild.currentResult}.",
                        attachLog: true,
                        attachmentsPattern: 'productionDeployment.txt'
                    )
                }
            }
        }
    }
}
