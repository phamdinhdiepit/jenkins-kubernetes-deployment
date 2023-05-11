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
      steps {
        withCredentials([kubeconfigContent(credentialsId: 'sss')]) {
    sh 'kubectl get node'
}
      }
    }

  }

}
