pipeline{
    agent any
    stages{
        stage("w=testing when condition"){
            environment{
                DEPLOY_TO = "prod"
            }
            when{
                environment name : "prod", value : "dev"
            }
            steps{
                echo "condition satified for $DEPLOY_TO environment"
            }
        }
    }
}
