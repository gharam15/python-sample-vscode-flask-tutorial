pipeline{
   agent{
        label "java"
   }

   stages{
     stage("Build java app"){
        steps{
            sh 'echo "start building java"'
        }
     }
     stage("Test java app"){
        steps{
            sh 'echo "Test java"'
        }
     }
     stage("Build image app"){
        steps{
            sh 'echo "build java image"'
        }
     }
   } 
}