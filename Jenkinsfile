// we have when condition using which we can run run stages if conditions are met
pipeline{
    agent any
    environment{
        DEPLOY_TO='prod'
    }
    
    stages{
        stage('deployment'){
            
            when{
                // environment name: 'DEPLOY_TO' , value: 'prod'
                equals expected: 9 , actual: "currentBild.number"
            }
            steps{
                echo 'Deploying...'
                echo "${BUILD_NUMBER}"
            }
        }
    }
}
        
