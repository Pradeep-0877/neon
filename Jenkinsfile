//expression
pipeline{
    agent any
    stages{
        stage('Build'){
            steps{
                echo "Welcomr to Build stage"
            }
        }
        stage('deploy to dev'){
            steps{
                echo "deployimg to dev environment"

            }
        }
        stage("deploy to stage"){
            when{
                //stage should execute with either production branch or staging branch
                expression{
                    BRANCH_NAME ==~ /(production|staging)/ //For using  BRANCH_NAME it should work in multibranch pipeline


                }
            }
            steps{
                echo "deploy to staging"
            }
        }
    }
}
