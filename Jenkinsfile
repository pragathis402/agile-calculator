pipeline {
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['V1', 'V2', 'V3', 'V4'], description: 'Select the Experiment Version')
    }
    stages {
        stage('Task 1: Checkout') {
            steps {
                echo "Running ${params.VERSION}..."
                // Simulating checkout from GitHub
                git 'https://github.com/your-repo/project.git'
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
                        sh 'touch status.txt'
                        echo 'status.txt created.'
                    } else if (params.VERSION == 'V4') {
                        sh 'echo "Pipeline Execution Completed" >> status.txt'
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
                        sh 'echo "Build Successful" > status.txt'
                        echo 'Status written to file.'
                    } else if (params.VERSION == 'V4') {
                        echo 'Final Content of status.txt:'
                        sh 'cat status.txt'
                    }
                }
            }
        }
    }
}
