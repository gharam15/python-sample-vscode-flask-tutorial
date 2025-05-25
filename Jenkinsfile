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
            sh "echo '${xyz}'"
            sh "docker build -t gharam/data:v${BUILD_NUMBER} ."
        }
     }
      stage("build Docker image"){
        steps{
            
            sh "docker push -t gharam/data:v${BUILD_NUMBER} ."
        }
     }
   } 
}