pipeline {
      agent any
      stages{
          stage('build'){
             steps{
                  echo " build stage called successfull"
                  sh './gradlew build --no-daemon'
                  archiveArtifacts artifacts : 'dist/trainSchedule.zip'
             }
          }
            stage('test'){
             steps{
                  echo " test stage called successfull"
             }
          }
      }
}
