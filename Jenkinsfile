pipeline{
    agent{
        label "k8s-slave"
    }
    stages{
        stage("Build"){
            environment{
                DEPLOY_TO = "dev"
            }
            when{
                // environment name: DEPLOY_TO, value: "prod"
                not{
                    equals expected: 13, actual: "$DEPLOY_TO"
                }
            }
            steps{
                echo "Building ...."
            }
        }
    }
}
