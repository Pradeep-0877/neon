pipeline{
    agent{
        label "k8s-slave"
    }
     environment{
                DEPLOY_TO = "dev"
    }
    stages{
        stage("Build"){
           
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
