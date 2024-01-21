pipeline{
    agent any
    stages{
        
        stage("A"){
          environment{
            DEPLOY_TO="PROD"
            myBool=true
            myNumber=18
          }
            steps{
                echo "DEPLOY_TO ${DEPLOY_TO}"
                echo "myBool ${myBool}"
                echo "myNumber ${myNumber}"
            }

        }
    }
}
