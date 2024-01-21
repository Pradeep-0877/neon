pipeline{
    agent any
    parameters[
        booleanParam(defaultValue: false, description: "Enable service", name: 'SELECT')
    ]
    stages{
        stage('A'){
            steps[
                echo "booleanParam is set to ${params.SELECT}"
            ]
        }
    }
}
