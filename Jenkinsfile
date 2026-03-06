pipeline {
    agent any

    stages {
        // --- VERSION 1: Basic Messaging ---
        stage('Version 1: Startup') {
            steps {
                echo '--- Executing Version 1 ---'
                git 'https://github.com/your-username/your-repo.git' // Task 1
                echo 'Pipeline execution has started.'             // Task 2
                echo 'Pipeline execution completed.'               // Task 3
            }
        }

        // --- VERSION 2: Processing Logic ---
        stage('Version 2: Processing') {
            steps {
                echo '--- Executing Version 2 ---'
                git 'https://github.com/your-username/your-repo.git' // Task 1
                echo 'Project files are being processed...'          // Task 2
                echo 'Processing completion reached.'                // Task 3
            }
        }

        // --- VERSION 3: File Creation ---
        stage('Version 3: Status Creation') {
            steps {
                echo '--- Executing Version 3 ---'
                git 'https://github.com/your-username/your-repo.git' // Task 1
                sh 'touch status.txt'                                // Task 2
                sh 'echo "Build Successful" > status.txt'            // Task 3
            }
        }

        // --- VERSION 4: File Append & Display ---
        stage('Version 4: Finalization') {
            steps {
                echo '--- Executing Version 4 ---'
                git 'https://github.com/your-username/your-repo.git' // Task 1
                sh 'echo "Pipeline Execution Completed" >> status.txt' // Task 2
                
                // Task 3: Display the contents of status.txt
                script {
                    def fileContent = readFile('status.txt')
                    echo "Final Status Report:\n${fileContent}"
                }
            }
        }
    }
    
    post {
        always {
            echo 'Experiment 11 Simulation Finished.'
        }
    }
}
