pipeline {
  agent { docker { image 'golang:1.17.5-alpine' } }
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
