pipeline {
    agent any
    
   
    
    stages {
        stage('Download Jenkinsfile from S3') {
            steps {
                script {
                    // Download Jenkinsfile from S3 bucket
                    sh "s3://buckerforsampleapp/Jenkinsfile"
                }
            }
        }
        
        stage('Build') {
            steps {
                // Execute the downloaded Jenkinsfile
                load 'Jenkinsfile'
            }
        }
    }
}
