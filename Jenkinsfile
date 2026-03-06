pipeline {
    agent any
    stages {
        stage('Version 2: Add Files') {
            steps {
                // Task 1: Checkout updated repository
                checkout scm
                
                // Task 2: Create two files inside the testfolder directory
                bat 'echo Hello Jenkins > testfolder\\file1.txt'
                bat 'echo Hello World > testfolder\\file2.txt'
                
                // Task 3: Display all files inside the directory
                bat 'dir testfolder'
            }
        }
    }
}
