pipeline {
  agent any

  tools {
    terraform 'terraform'
  }

  environment {
    AWS_ACCESS_KEY_ID     = credentials('aws-secret-key-id')
    AWS_SECRET_ACCESS_KEY = credentials('aws-secret-access-key')
  }

  stages {
    stage('Init Provider') {
      steps {
        sh 'terraform init'
      }
    }
    stage('Plan Resources') {
      steps {
        sh 'terraform plan'
      }
    }
  }
}
