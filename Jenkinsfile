pipeline{
   agent{
        label "java"
   }
   environment{
      xyz='ITI'
   }
   stages{
     stage("build Docker image"){
        steps{
            sh "echo '${xyz}'"
            sh "docker build -t python:v${BUILD_NUMBER} ."
        }
     }
   } 
}