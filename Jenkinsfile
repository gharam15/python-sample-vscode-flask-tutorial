pipeline{
   agent{
        label "java"
   }
   environment{
      xyz='Data'
   }
   stages{
     stage("build Docker image"){
        steps{
            sh "echo'${xyz}'"
            sh "docker build -t python:v${BUILD_NUMBER} ."
        }
     }
   } 
}