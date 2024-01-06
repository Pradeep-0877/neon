// we have when condition using which we can run run stages if conditions are met
pipeline{
    agent any
    
    stages{
        stage('deployment'){
            environment{
                DEPLOY_TO='prod'
            }
            when{
                environment name: 'DEPLOY_TO' , value: 'prod'
            }
            steps{
                echo 'Deploying...'
            }
        }
    }
}
        
