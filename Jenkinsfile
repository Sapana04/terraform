pipeline {
    agent any

    stages {

        stage('Terraform Version') {
            steps {
                sh 'terraform version'
            }
        }

        stage('AWS Check') {
            steps {
                sh 'aws sts get-caller-identity --no-cli-pager'
            }
        }

        stage('Terraform Init') {
            steps {
                sh 'terraform init'
            }
        }

        stage('Terraform Plan') {
            steps {
                sh 'terraform plan'
            }
        }

        stage('Terraform Apply') {
            steps {
                sh 'terraform apply -auto-approve'
            }
        }

    }
}