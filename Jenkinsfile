pipeline{
    agent any
    parameters{
        booleanParam(defaultValue: false, name: "SELECT", description: "Using scrip[t...]")
    }
    stages{
        stage("A"){
            steps{
                script{
                    if(params.SELECT==false){
                        currentBuild.result='SUCCESS'
                        return
                    }
                    else{
                        echo "The select parameter is true "
                    }

                }

            }
        }
    }
}
