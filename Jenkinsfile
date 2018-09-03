pipeline {
    agent any
	
	tools { 
        maven 'Maven 3.5.4' 
        jdk 'jdk8' 
    }
    stages{
	
		stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = ${PATH}"
                    					
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