pipeline {
    agent any
    stages{
        stage('Build'){
            steps {
                bat 'localMaven clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }
       
    }
}