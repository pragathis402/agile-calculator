pipeline {
    agent any

    stages {
        stage('Version 2: Add Files') {
            steps {
                // Task 1: Checkout updated repository
                checkout scm
                
                // Task 2: Create the directory first (fixes the "path not found" error)
                // Then create the two files
                bat 'if not exist testfolder mkdir testfolder'
                bat 'echo Hello Jenkins > testfolder\\file1.txt'
                bat 'echo World > testfolder\\file2.txt'
                
                // Task 3: Display all files inside the directory
                bat 'dir testfolder'
            }
        }
    }
}
