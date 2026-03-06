pipeline {
    agent any
   stage('Version 2: Add Files') {
    steps {
        checkout scm
        
        // FIX: Ensure the directory exists first
        bat 'if not exist testfolder mkdir testfolder'
        
        // Task 2: Create two files inside the testfolder directory
        // Use double backslashes for Jenkins paths
        bat 'echo Hello Jenkins > testfolder\\file1.txt'
        bat 'echo Hello World > testfolder\\file2.txt'
        
        // Task 3: Display all files inside the directory
        bat 'dir testfolder'
    }
}
}
