pipeline {
    agent any
    
   
    
    stages {
        stage('Download Jenkinsfile from S3') {
            steps {
                script {
                    // Download Jenkinsfile from S3 bucket
                    sh "aws s3 cp s3://buckerforsampleapp/Jenkinsfile /opt/Jenkinsfile"
                }
            }
        }
        
        stage('Build') {
            steps {
                script {
                // Execute the downloaded Jenkinsfile
                load "/opt/Jenkinsfile"
                }
            }
        }
    }
}
