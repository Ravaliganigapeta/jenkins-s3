pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/Ravaliganigapeta/jenkins-s3.git'
            }
        }
        stage('Terraform Init') {
            steps {
                sh "terraform init"
            }
        }
        stage('Terraform Plan') {
            steps {
               // Generate an execution plan
                  sh 'terraform plan'
      }    
    }
        stage('Terraform Action') {
            steps {
                   sh 'terraform apply -auto-approve'
            }
        }
    }
}


