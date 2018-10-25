pipeline {
	/*New update*/
    agent any
    stages{
        stage('Build'){
		
            steps {
				echo 'Got to steps'
                bat 'mvn clean package'
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
