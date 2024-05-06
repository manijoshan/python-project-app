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
	stage('Test_And_Deploy') {
             steps {
                sh 'chmod +x start.sh'
                sh 'bash start.sh'
            }
        }

    }
 
}





