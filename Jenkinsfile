pipeline{
   agent{
        label "java"
   }

   stages{
     stage("Build java app"){
        steps{
            tool name: 'java-8', type: 'jdk'
            sh 'mvn clean package install'
        }
     }
     stage("Test java app"){
        steps{
            sh 'mvn test'
        }
     }
     stage("Build java image app"){
        steps{
            sh 'docker build -t java:v1 .'
        }
     }
   } 
}