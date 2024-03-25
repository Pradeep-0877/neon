pipeline{
    agent any
    stages{
        stage("running parellel stages"){
            parellel{
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
