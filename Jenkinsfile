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
	stage('Artifact_Generator') {
            steps {
                sh 'chmod +x artifact.sh'
                sh 'bash artifact.sh'
            }
	}	
	stage('Test_&_Deploy') {
             steps {
                sh 'chmod +x start.sh'
                sh 'bash start.sh'
            }
        }

    }

}





