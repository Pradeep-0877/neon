pipeline{
    agent any
    stages{
        stage("running parellel stages"){
            parallel{
                stage("sonar"){
                    steps{
                        echo "sonar scans successfull...."
                    }
                }
                stage("fortify scans"){
                    steps{
                        echo "fortify scans completed"
                    }
                }
            }
        }
    }

}
