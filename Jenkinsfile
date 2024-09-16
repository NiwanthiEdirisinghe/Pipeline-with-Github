pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project'
            }
            post {
                always {
                    script {
                        // Capture the console log and save it as a file
                        def consoleLog = currentBuild.rawBuild.getLog().join("\n")
                        writeFile file: 'consoleLog.txt', text: consoleLog
                        // Send the email with the log as an attachment
                        emailext attachLog: true,
                                 attachmentsPattern: 'consoleLog.txt',
                                 to: 'niwanthiedirisinghe.95@gmail.com',
                                 subject: "Build Stage Status: ${currentBuild.currentResult}",
                                 body: """The Build stage has completed with status: ${currentBuild.currentResult}.
                                 \n\nPlease find the console log attached."""
                    }
                }
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests'
            }
            post {
                always {
                    script {
                        def consoleLog = currentBuild.rawBuild.getLog().join("\n")
                        writeFile file: 'consoleLog.txt', text: consoleLog
                        emailext attachLog: true,
                                 attachmentsPattern: 'consoleLog.txt',
                                 to: 'niwanthiedirisinghe.95@gmail.com',
                                 subject: "Unit and Integration Tests Status: ${currentBuild.currentResult}",
                                 body: """The Unit and Integration Tests stage has completed with status: ${currentBuild.currentResult}.
                                 \n\nPlease find the console log attached."""
                    }
                }
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Analyzing code'
            }
            post {
                always {
                    script {
                        def consoleLog = currentBuild.rawBuild.getLog().join("\n")
                        writeFile file: 'consoleLog.txt', text: consoleLog
                        emailext attachLog: true,
                                 attachmentsPattern: 'consoleLog.txt',
                                 to: 'niwanthiedirisinghe.95@gmail.com',
                                 subject: "Code Analysis Status: ${currentBuild.currentResult}",
                                 body: """The Code Analysis stage has completed with status: ${currentBuild.currentResult}.
                                 \n\nPlease find the console log attached."""
                    }
                }
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Performing Security Scan'
            }
            post {
                always {
                    script {
                        def consoleLog = currentBuild.rawBuild.getLog().join("\n")
                        writeFile file: 'consoleLog.txt', text: consoleLog
                        emailext attachLog: true,
                                 attachmentsPattern: 'consoleLog.txt',
                                 to: 'niwanthiedirisinghe.95@gmail.com',
                                 subject: "Security Scan Status: ${currentBuild.currentResult}",
                                 body: """The Security Scan stage has completed with status: ${currentBuild.currentResult}.
                                 \n\nPlease find the console log attached."""
                    }
                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging'
            }
            post {
                always {
                    script {
                        def consoleLog = currentBuild.rawBuild.getLog().join("\n")
                        writeFile file: 'consoleLog.txt', text: consoleLog
                        emailext attachLog: true,
                                 attachmentsPattern: 'consoleLog.txt',
                                 to: 'niwanthiedirisinghe.95@gmail.com',
                                 subject: "Deploy to Staging Status: ${currentBuild.currentResult}",
                                 body: """The Deploy to Staging stage has completed with status: ${currentBuild.currentResult}.
                                 \n\nPlease find the console log attached."""
                    }
                }
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Integration Tests on Staging'
            }
            post {
                always {
                    script {
                        def consoleLog = currentBuild.rawBuild.getLog().join("\n")
                        writeFile file: 'consoleLog.txt', text: consoleLog
                        emailext attachLog: true,
                                 attachmentsPattern: 'consoleLog.txt',
                                 to: 'niwanthiedirisinghe.95@gmail.com',
                                 subject: "Integration Tests on Staging Status: ${currentBuild.currentResult}",
                                 body: """The Integration Tests on Staging stage has completed with status: ${currentBuild.currentResult}.
                                 \n\nPlease find the console log attached."""
                    }
                }
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production'
            }
            post {
                always {
                    script {
                        def consoleLog = currentBuild.rawBuild.getLog().join("\n")
                        writeFile file: 'consoleLog.txt', text: consoleLog
                        emailext attachLog: true,
                                 attachmentsPattern: 'consoleLog.txt',
                                 to: 'niwanthiedirisinghe.95@gmail.com',
                                 subject: "Deploy to Production Status: ${currentBuild.currentResult}",
                                 body: """The Deploy to Production stage has completed with status: ${currentBuild.currentResult}.
                                 \n\nPlease find the console log attached."""
                    }
                }
            }
        }
    }
}
