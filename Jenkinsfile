pipeline{
    agent any
    parameters{
        booleanParam(defaultValue: false, description: "Perform sonar", name: 'SONAR')
        string(defaultValue: PROD, description: 'Select to Environment',required: true,name: DEPLOY_TO)
    }
    stages{
        stage('A'){
            steps{
                echo "booleanParam is set to ${params.SELECT}"
            }
        }
    }
}
