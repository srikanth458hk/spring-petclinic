pipeline {
    agent any
    
   
    
    stages {
        stage('Download Jenkinsfile from S3') {
            steps {
                script {
                    // Download Jenkinsfile from S3 bucket
                    sh "aws s3 cp s3://buckerforsampleapp/Jenkinsfile /tmp/Jenkinsfile"
                }
            }
        }
        
        stage('Build') {
            steps {
                // Execute the downloaded Jenkinsfile
                load '/tmp/Jenkinsfile'
                
            }
        }
    }
}
