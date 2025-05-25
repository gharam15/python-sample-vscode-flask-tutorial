node('java'){
    checkout scm
    stage('build Docker image'){
        sh "docker build gharam/data:v${BUILD_NUMBER} ."
    }
    stage("Push Docker image"){
        sh "docker push gharam/data:v${BUILD_NUMBER}"
        }

}