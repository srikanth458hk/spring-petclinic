pipeline {
  agent any

  stages {
    stage('Checkout') {
      steps {
        // Checkout the code from the repository
        checkout scm
      }
    }

    stage('Call Jenkinsfile') {
      steps {
        // Call Jenkinsfile from the other repository
        script {
          git 'https://https://github.com/srikanth458hk/jenkinsfilerepo.git'
          load 'Jenkinsfile'
        }
      }
    }
  }
}

