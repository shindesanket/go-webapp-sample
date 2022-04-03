pipeline {
  agent any
  tools {
    go 'go-1.17'
  }
  
  environment {
    GO111MODULE='on'
  }
  stages {
    stage('build') {
      steps {
        git 'https://github.com/AdminTurnedDevOps/go-webapp-sample.git'
        sh 'go build .'
        sh './go-webapp-sample'
      }
    }
        stage('run') {
      steps {
        sh 'cd /var/lib/jenkins/workspace/SampleGoPipeline && SampleGoPipeline &'
      }
    }

  }
}
