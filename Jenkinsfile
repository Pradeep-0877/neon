pipeline{
    agent any
     environment{
                DEPLOY_TO = "dev"
     }
    stages{
        stage("Deploy to dev"){
           
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
