pipeline {
    agent any 
    stages {
        stage ('git-checkout') {
            steps {
                cleanWs()
                sh '''
                git clone -b $branches $GITURL
                '''
            }
        }
        stage ('maven-build') {
            steps {
                sh '''
                cd hello-world
                mvn clean install
                '''
            }
        }
    }
    post {
        always {
            cleanWs()
        }
    }
} 
