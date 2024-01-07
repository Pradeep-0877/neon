pipeline{
    agent any
    stages{
        stage('parellel stages'){
            parellel{
                stage("executing sonar scan"){
                    steps[
                        echo "doing sonar scans"
                    ]
                }
                stage("Doing forify scans"){
                    steps[
                        echo "Doing fortify scans"
                        sleep 20
                    ]
                }
                stage("exucuting checkmarx scan"){
                    steps{
                        echo "exucuting checkmarx scan"
                        sleep 10
                    }
                }

            }
        }
    }
}
