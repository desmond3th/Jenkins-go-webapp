pipeline{
  agent: any
  tools{
    go 'go-1.21'
  }

  environment{
    GO111MODULE='on'
  }

  stages{
    stage('Development'){
      steps{
        git 'https://github.com/desmond3th/Jenkins-go-webapp.git'
      }
    }

    stage('Building images'){
      steps{
        script{
          app = docker.build("jenkins-go-webapp/go-webapp-sample")
        }
      }
  }
}