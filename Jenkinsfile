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
            when{
                branch 'master' 
            }
            steps{
                input 'Does the staging environment look OK?'
                milestone(1)
                echo 'deploy to production server only if branch is master'
            }
        }

    }
}
