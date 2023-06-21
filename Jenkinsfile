pipeline {
  agent any
  
  environment {
    AWS_DEFAULT_REGION = 'us-east-1'  // Set your desired AWS region
  }
  
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/Ravaliganigapeta/jenkins-s3.git'
         }
      }
   }
   stage('Provision S3 Bucket') {
      steps {
         dir('terraform') {
            sh 'terraform init'
              }
          }
      }
  }
    
