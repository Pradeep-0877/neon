pipeline{
    agent any
    options{
        buildDiscarder(logRotator(numToKeepStr: '2')) 
    }
    parameters{
        // string ,text, booleanparameter, choice, password these some types parameters we can use
        string(name: 'PERSON', defaultValue: 'pradeep', description: 'Who should I say hello to?')
        string(name: "BRANCH_NAME", defaultValue: "main", description: "In which branch should i Build ?")
        booleanParam( name: "TOGGLE", defaultValue: true, description: "Toggle this Value ?")
        choice(name: "ENV", choices: ['Stage','Test','Prod'], description: "Choose any of the Deployment")
    }
    stages{
        stage("parameters example"){
            steps{
                echo "name is  ${params.PERSON}"
                echo "Deploy to ${params.ENV}"
                echo "toggling ${params.TOGGLE}"
            }
        }
    }
}
