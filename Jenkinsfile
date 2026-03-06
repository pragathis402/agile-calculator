pipeline {
    agent any

    stages {
        // Version 1 Tasks
        stage('V1: Initialization') {
            steps {
                // Task 1: Already handled by Jenkins auto-checkout
                echo "Task 1: Project checked out successfully."
                echo "Task 2: Pipeline execution has started"
                echo "Task 3: Pipeline execution completed (V1)"
            }
        }

        // Version 2 Tasks
        stage('V2: File Processing') {
            steps {
                echo "Task 1: Using updated repository files..."
                echo "Task 2: Project files are being processed..."
                echo "Task 3: Processing completion reached."
            }
        }

        // Version 3 Tasks
        stage('V3: Status Creation') {
            steps {
                echo "Task 1: Accessing latest repository state..."
                echo "Task 2: Creating status.txt..."
                // Use 'bat' for Windows paths seen in your log, or 'sh' for Linux
                bat 'echo. > status.txt' 
                echo "Task 3: Writing Build Successful to file..."
                bat 'echo Build Successful > status.txt'
            }
        }

        // Version 4 Tasks
        stage('V4: Logging & Output') {
            steps {
                echo "Task 1: Final repository sync check..."
                echo "Task 2: Appending completion message..."
                bat 'echo Pipeline Execution Completed >> status.txt'
                echo "Task 3: Displaying final contents of status.txt:"
                bat 'type status.txt'
            }
        }
    }
    
    post {
        always {
            echo "All experimental versions have been executed."
        }
    }
}
