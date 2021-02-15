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
           git branch: 'master', credentialsId: '204c40a298982e278e342bb6d3f0fb2831ad899f', url: 'git@github.com:/surajm2021/cicd-pipeline-train-schedule-pipelines/blob/master/Jenkinsfile'
        }

    }
}
