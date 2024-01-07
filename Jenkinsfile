pipeline{
    agent any
    stages{
        stage('parellel stages'){
            parallel{
                stage("executing sonar scan"){
                    steps{
                        echo "exucuting sonar scans"
                        sleep 10
                    }
                }
                stage("Doing forify scans"){
                    steps{
                        echo "Doing fortify scans"
                        sleep 20
                    }
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
