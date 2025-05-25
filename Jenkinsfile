node('java') {
    checkout scm

    stage('Build Docker image') {
        sh "docker build -t gharam/iti:v${BUILD_NUMBER} ."
    }

    stage("Push Docker image") {
        sh "docker push gharam/iti:v${BUILD_NUMBER}"
    }
}
