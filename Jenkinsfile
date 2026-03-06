pipeline {
    agent any

    stages {
        // --- VERSION 1 ---
        stage('Version 1: Startup') {
            steps {
                echo '--- Executing Version 1 ---'
                checkout scm                                    // Task 1: Uses your actual GitHub repo
                echo 'Pipeline execution has started.'          // Task 2
                echo 'Pipeline execution completed.'            // Task 3
            }
        }

        // --- VERSION 2 ---
        stage('Version 2: Processing') {
            steps {
                echo '--- Executing Version 2 ---'
                checkout scm                                    // Task 1
                echo 'Project files are being processed...'       // Task 2
                echo 'Processing completion reached.'             // Task 3
            }
        }

        // --- VERSION 3 ---
        stage('Version 3: Status Creation') {
            steps {
                echo '--- Executing Version 3 ---'
                checkout scm                                    // Task 1
                bat 'if not exist status.txt type nul > status.txt' // Task 2: Windows command to create file
                bat 'echo Build Successful > status.txt'         // Task 3
            }
        }

        // --- VERSION 4 ---
        stage('Version 4: Finalization') {
            steps {
                echo '--- Executing Version 4 ---'
                checkout scm                                    // Task 1
                bat 'echo Pipeline Execution Completed >> status.txt' // Task 2: Append
                
                // Task 3: Display the contents
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
