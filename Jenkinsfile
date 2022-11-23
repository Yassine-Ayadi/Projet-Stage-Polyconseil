#!/usr/bin/env groovy

pipeline {
    agent any
  
    environment {
        AWS_ACCESS_KEY_ID = credentials('jenkins_aws_access_key_id')
        AWS_SECRET_ACCESS_KEY = credentials('jenkins_aws_secret_access_key')
    }
  
    stages {
      
        stage('provision infrastructure') {

            steps {
                script {
                    dir('Terraform') {
                       // sh "terraform init" 
                       // sh "terraform apply --auto-approve" 
                       //sh "aws eks update-kubeconfig --name myapp-eks-cluster --region eu-west-3"
                        sh "terraform delete --auto-approve"
                    }
                }
            }
        } 
      
    /*    stage('deploy Wordpress Helm Chart') {
            steps {
                script {
                       sh "helm install wordpress ./Wordpress_Helm_Chart "              

                }
            }
        } */


    }
}

