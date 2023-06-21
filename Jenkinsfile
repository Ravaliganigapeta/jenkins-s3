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
        stage('Terraform Action') {
            steps {
                input(message: 'Click "proceed" to approve the above Terraform Plan')
                sh(
                    label:  'Terraform Apply',
                    script: 'terraform ${action} --auto-approve'
                )
                //sh "terraform ${action} --auto-approve"   
            }
        }
    }
}

