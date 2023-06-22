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
                sh "terraform init -backend-config='access_key'='AKIARZKPS5HWFBQX4EVG' -backend-config='secret_key'='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'"
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


