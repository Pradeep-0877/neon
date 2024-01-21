pipeline{
    agent any
    stages{
        environment{
            DEPLOY_TO="PROD"
            myBool=true
            myNumber=18
        }
        stage("A"){
            steps{
                echo "DEPLOY_TO ${DEPLOY_TO}"
                echo "myBool ${myBool}"
                echo "myNumber ${myNumber}"
            }

        }
    }
}
