pipeline {
    agent any
	
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