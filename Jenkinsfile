pipeline{
    agent any
    parameters{
        booleanParam(defaultValue: false, description: "Perform sonar", name: 'SONAR')
        string(defaultValue: "PROD", description: 'Select to Environment',name: "DEPLOY_TO")
        choice(choices: ["TEST","PROD","QA"],description: "deploy environment",name: "DEPLOY_TO_CHOICES")
    }
    stages{
        stage('A'){
            steps{
                echo "environment is is set to ${params.DEPLOY_TO_CHOICES}"
            }
        }
    }
}
