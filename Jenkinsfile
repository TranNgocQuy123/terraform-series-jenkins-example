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
        echo 'Testing'
        //sh 'terraform init'
      }
    }
    stage('Plan Resources') {
      steps {
        echo 'Testing'
        // sh 'terraform plan'
      }
    }
    stage('Apply Resources'){
      steps {
       echo 'Testing'
       // sh 'terraform apply -auto-approve'
      }
    }
    stage('Destroy'){
      steps {
        sh 'terraform destroy -auto-approve'
      }
    }
  }
}
