pipeline {
    agent { 
        label "agentfarm"
    }
    stages {
        stage('Build') {
            steps {
                sh 'chmod +x build.sh'
                sh 'bash build.sh'
            }
        }
	stage('Generate_Artifact') {
            steps {
                sh 'chmod +x artifact.sh'
                sh 'bash artifact.sh'
            }
	}	
	stage('Test_And_Deploy') {
             steps {
                sh 'chmod +x start.sh'
                sh 'bash start.sh'
            }
        }

    }
   post {
     always {
       archiveArtifacts artifacts: 'dist/*.tar.gz', fingerprint: true
    }
  }
}





