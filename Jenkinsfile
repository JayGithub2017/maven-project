pipeline {
    agent any
	
	tools { 
        localMaven 'Maven 3.5.4' 
            }
    stages{
	
		stage ('Initialize') {
            steps {
                bat '''
                    echo "PATH = ${PATH}"
					'''
					}
        }
                    					
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