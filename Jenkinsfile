pipeline{
    agent any
    stages{
        stage("Deploy to dev"){
            environment{
                DEPLOY_TO = "dev"
            }
            when{
                anyOf{
                    branch 'production'
                    environment name: "DEPLOY_TO", value: "dev"
                }
            }
            steps{
                echo "deployed to $DEPLOY_TO"
            }
        }
    }
}
