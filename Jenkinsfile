pipeline {
    agent any

    }
    stages {
        stage('vcs') {
            steps {
                git branch: 'main', url: 'https://github.com/WorkshopsByKhaja/saleor-dashboard.git'
            }
        }
        stage('build') {
            steps {
                sh 'mvn package'
            }
        }

    }
}    