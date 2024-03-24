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
                equals expected: 13, actual: "$BUILD_NUMBER"
            }
            steps{
                echo "Building ...."
            }
        }
    }
}
