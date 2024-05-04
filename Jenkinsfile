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
    }
}

