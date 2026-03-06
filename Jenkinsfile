pipeline {
    agent any
    stages {
        stage('Version 3') {
            steps {
                checkout scm
                bat 'if not exist testfolder mkdir testfolder'
                // Task 2: Copy operation
                bat 'copy README.md testfolder\\'
                // Task 3: Verify
                bat 'dir testfolder'
            }
        }
    }
}
