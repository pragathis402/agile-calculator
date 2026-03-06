pipeline {
    agent any
    stages {
        stage('Version 1') {
            steps {
                // Task 1: Checkout
                checkout scm 
                
                // Task 2: Create directory
                bat 'mkdir testfolder'
                
                // Task 3: Verify
                bat 'dir'
            }
        }
    }
}
