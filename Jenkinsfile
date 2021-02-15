pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running build automation'
            
            }
        }
        stage('deploy to test server') {
            steps{
                   echo 'deploy to test server'
            }
        }
        stage('deploy to production server'){
            steps{
                input 'Does the staging environment look OK?'
                milestone(1)
                echo 'deploy to production server only if branch is master'
            }
        }
        stage('Example Username/Password') {
            environment {
                SERVICE_CREDS = credentials('github_key')
            }
            steps {
                sh 'echo "Service user is $SERVICE_CREDS_USR"'
                sh 'echo "Service password is $SERVICE_CREDS_PSW"'
                sh 'curl -u $SERVICE_CREDS https://myservice.example.com'
            }
        }

    }
}
