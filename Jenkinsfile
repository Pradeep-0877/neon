//Post:- This is used to execute one or more steps that needs to be executed post the completion  of our pipeline or tsgae build 
// It can be defined in pipeline evel as well as stage level as well
//condition blocks: always, changed, fixed, regression, aborted, failure, success, unstable, unsuccessful, and cleanup. These 
//condition blocks allow the execution of steps 
//inside each condition depending on the completion 
//status of the Pipeline or stage. The condition blocks are executed in the order shown below.
pipeline{
    agent any
    options{
        buildDiscarder(logRotator(numToKeepStr: '2'))
    }
    stages{
        stage("My Build"){
            steps{
                echo "creating a build"
                error "This is just an error"
            }

        }
       
    }
     post{
        //This will only execute if the pipeline has a success message

        success{
            echo "This means the pipeline is successfull"
        }
        failure{
            echo "This will only execute if the pipeline/stage has a failure"
        }
        always{
            // Mail notification is typically used here
            echo "This block is printed always"
        }
            
    }
}
