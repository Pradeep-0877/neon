pipeline{
    agent{
        label 'k8s-slave'
    }
    environment{
        DEPLOY_TO = 'dev'
    }
    stages[
        stage("Deploy"){
            when{
                expression{
                    BRANCH_NAME ==~ /(dev|test)/
                }
            }
            steps{
                echo "deploying to $BRANCH_NAME env"
            }
        }
        stage("Deploy to prod"){
            when{
                expression{
                    BRANCH_NAME ==~ /(prod|hotfix)/
                }
            }
            steps{
                echo "Deploying in $BRANCH_NAME"
            }
        }
    ]
}
