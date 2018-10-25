pipeline {
	/*New update*/
    agent any
    stages{
        stage('Build'){
		echo 'Got to steps'
            steps {
                sh 'mvn clean package'
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
