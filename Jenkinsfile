pipeline{
    agent any
    options{
        buildDiscarder(logRotator(numToKeepStr: '2')) }
    }
    parameters{
        // string ,text, booleanparameter, choice, password these some types parameters we can use
        string(name: 'PERSON', defaultValue: 'pradeep', description: 'Who should I say hello to?')
        string(name: "BRANCH_NAME", defaultValue: "main", description: "In which branch should i Build ?")
    }
    stages{
        stage("parameters example"){
            steps{
                echo "name is  ${params.PERSON}"
            }
        }
    }
}
