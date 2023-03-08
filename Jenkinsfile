pipeline {
    agent any 
    stages {
        stage ('git-checkout') {
            steps {
                cleanWs()
                sh '''
                git clone -b master https://github.com/hemanthkatkozu/terraform-aws-ec2-instance.git
                '''
            }
        }
        /*stage ('maven-build') {
            steps {
                sh '''
                cd hello-world
                mvn clean install
                '''
            }
        }*/
    }
    post {
        always {
            cleanWs()
        }
    }
} 
