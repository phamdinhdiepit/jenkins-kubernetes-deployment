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
      withKubeConfig([credentialsId: 'sss']) {
       sh 'curl -LO "https://storage.googleapis.com/kubernetes-release/release/v1.20.5/bin/linux/amd64/kubectl"'  
        sh 'chmod u+x ./kubectl'  
        sh './kubectl get node'
    }
      }
    }

  }

}
