pipeline{
    agent any
    environment{
        DEPLOY_TO="prod"
    }
    stages{
        stage('Build'){
            when{
                anyOf{
                    //the below all conditions needs to be satisfied in order for the stage to execute
                    branch 'feature'
                    environment name: 'DEPLOY_TO', value: 'prods'
                }
            }
            steps{
                echo "Hurray!! it's working fine"
            }

        }
    }
}
