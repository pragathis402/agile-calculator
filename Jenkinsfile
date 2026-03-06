pipeline {
    agent any

    stages {
        // Version 1 Tasks
        stage('V1: Initialization') {
            steps {
                echo "Task 1: Checking out project..."
                git 'https://github.com/your-repo/project.git'
                echo "Task 2: Pipeline execution has started"
                echo "Task 3: Pipeline execution completed (V1)"
            }
        }

        // Version 2 Tasks
        stage('V2: File Processing') {
            steps {
                echo "Task 1: Checking out updated repository..."
                // Git checkout is usually handled at the start, but represented here for the task
                echo "Task 2: Project files are being processed..."
                echo "Task 3: Processing completion reached."
            }
        }

        // Version 3 Tasks
        stage('V3: Status Creation') {
            steps {
                echo "Task 1: Checking out latest repository..."
                echo "Task 2: Creating status.txt..."
                sh 'touch status.txt'
                echo "Task 3: Writing Build Successful to file..."
                sh 'echo "Build Successful" > status.txt'
            }
        }

        // Version 4 Tasks
        stage('V4: Logging & Output') {
            steps {
                echo "Task 1: Checking out updated repository..."
                echo "Task 2: Appending completion message..."
                sh 'echo "Pipeline Execution Completed" >> status.txt'
                echo "Task 3: Displaying final contents of status.txt:"
                sh 'cat status.txt'
            }
        }
    }
    
    post {
        always {
            echo "All experimental versions have been executed."
        }
    }
}
