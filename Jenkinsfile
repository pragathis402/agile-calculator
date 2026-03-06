pipeline {
    agent any

    stages {
        stage('Version 4: Deletion') {
            steps {
                // Task 1: Checkout updated repository
                checkout scm
                
                // Task 2: Delete the directory using BAT
                // /s = Removes all directories and files in the specified directory
                // /q = Quiet mode, do not ask for confirmation
                bat 'if exist testfolder rd /s /q testfolder'
                
                // Task 3: Confirm removal
                // We use 'dir' to list the workspace. 'testfolder' should be missing.
                echo "Confirming directory removal..."
                bat 'dir'
            }
        }
    }
}
