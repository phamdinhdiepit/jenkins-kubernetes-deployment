pipeline {

  environment {
    dockerimagename = "diepphamit/react-app"
    dockerImage = ""
  }

  agent any

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/phamdinhdiepit/jenkins-kubernetes-deployment.git'
      }
    }

    

    stage('Deploying React.js container to Kubernetes') {
      steps{
      swithKubeConfig([credentialsId: 'sss', serverUrl: 'https://192.168.49.2:8443']) {
      sh 'kubectl get node'
    }
      }
    }

  }

}
