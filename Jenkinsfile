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
             
                echo 'deploy to production server only if branch is master'
            }
        }
        stage('Checkout') {
            steps{
                 git branch: 'master', credentialsId: 'jkey', url: 'git@github.com:/surajm2021/cicd-pipeline-train-schedule-pipelines/blob/master/Jenkinsfile'
             }
        }
    }
}
