pipeline {
    agent any
    stages {
        stage('Version 3: Copy Files') {
            steps {
                checkout scm
                // Ensure folder exists, then copy
                bat 'if not exist testfolder mkdir testfolder'
                bat 'copy README.md testfolder\\'
                
                // Verify
                bat 'dir testfolder'
            }
        }
    }
}S
