pipeline{
    agent any
    parameters{
        booleanParam(defaultValue: false, name: "SELECT", descption: "Using scrip[t...]")
    }
    stages{
        stege("A"){
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
