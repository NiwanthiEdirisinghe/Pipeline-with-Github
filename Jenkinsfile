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
                    archiveArtifacts artifacts: 'buildLog.txt', onlyIfSuccessful: true
                    sh '''
                    echo "The Build stage has completed with status: ${currentBuild.currentResult}." | mail -s "Build Stage Status: ${currentBuild.currentResult}" -A buildLog.txt niwanthiedirisinghe.95@gmail.com
                    '''
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
                    archiveArtifacts artifacts: 'testResults.txt', onlyIfSuccessful: true
                    sh '''
                    echo "The Unit and Integration Tests stage has completed with status: ${currentBuild.currentResult}." | mail -s "Unit and Integration Tests Status: ${currentBuild.currentResult}" -A testResults.txt niwanthiedirisinghe.95@gmail.com
                    '''
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
                    archiveArtifacts artifacts: 'codeAnalysis.txt', onlyIfSuccessful: true
                    sh '''
                    echo "The Code Analysis stage has completed with status: ${currentBuild.currentResult}." | mail -s "Code Analysis Status: ${currentBuild.currentResult}" -A codeAnalysis.txt niwanthiedirisinghe.95@gmail.com
                    '''
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
                    archiveArtifacts artifacts: 'securityScan.txt', onlyIfSuccessful: true
                    sh '''
                    echo "The Security Scan stage has completed with status: ${currentBuild.currentResult}." | mail -s "Security Scan Status: ${currentBuild.currentResult}" -A securityScan.txt niwanthiedirisinghe.95@gmail.com
                    '''
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
                    archiveArtifacts artifacts: 'stagingDeployment.txt', onlyIfSuccessful: true
                    sh '''
                    echo "The Deploy to Staging stage has completed with status: ${currentBuild.currentResult}." | mail -s "Deploy to Staging Status: ${currentBuild.currentResult}" -A stagingDeployment.txt niwanthiedirisinghe.95@gmail.com
                    '''
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
                    archiveArtifacts artifacts: 'stagingTests.txt', onlyIfSuccessful: true
                    sh '''
                    echo "The Integration Tests on Staging stage has completed with status: ${currentBuild.currentResult}." | mail -s "Integration Tests on Staging Status: ${currentBuild.currentResult}" -A stagingTests.txt niwanthiedirisinghe.95@gmail.com
                    '''
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
                    archiveArtifacts artifacts: 'productionDeployment.txt', onlyIfSuccessful: true
                    sh '''
                    echo "The Deploy to Production stage has completed with status: ${currentBuild.currentResult}." | mail -s "Deploy to Production Status: ${currentBuild.currentResult}" -A productionDeployment.txt niwanthiedirisinghe.95@gmail.com
                    '''
                }
            }
        }
    }
}
