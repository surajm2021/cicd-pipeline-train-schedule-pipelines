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
                 withCredentials([usernamePassword(credentialsId: 'git_hub_login', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                 
                  sh 'echo $PASSWORD'
                  
                  echo USERNAME
                  sh 'git clone https://github.com/surajm2021/shirapur-website'
                  echo "username is $USERNAME"
                }
             }
        }
    }
}
