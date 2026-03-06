pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['V1', 'V2', 'V3', 'V4'], description: 'Select the Experiment Version')
    }
    stages {
        stage('Task 1: Checkout') {
            steps {
                echo "Running ${params.VERSION}..."
                // Using your actual working repository
                git 'https://github.com/pragathis402/agile-calculator.git'
            }
        }
        
        stage('Task 2: Process/Action') {
            steps {
                script {
                    if (params.VERSION == 'V1') {
                        echo 'Pipeline execution has started.'
                    } else if (params.VERSION == 'V2') {
                        echo 'Project files are being processed.'
                    } else if (params.VERSION == 'V3') {
                        // Using 'powershell' because your logs show you are on Windows
                        powershell 'New-Item -Path . -Name "status.txt" -ItemType "file" -Force'
                        echo 'status.txt created.'
                    } else if (params.VERSION == 'V4') {
                        powershell 'Add-Content -Path status.txt -Value "Pipeline Execution Completed"'
                        echo 'Message appended.'
                    }
                }
            }
        }

        stage('Task 3: Status/Completion') {
            steps {
                script {
                    if (params.VERSION == 'V1') {
                        echo 'Pipeline execution completed.'
                    } else if (params.VERSION == 'V2') {
                        echo 'Processing completion.'
                    } else if (params.VERSION == 'V3') {
                        powershell 'Set-Content -Path status.txt -Value "Build Successful"'
                        echo 'Status written to file.'
                    } else if (params.VERSION == 'V4') {
                        echo 'Final Content of status.txt:'
                        powershell 'Get-Content status.txt'
                    }
                }
            }
        }
    }
}
