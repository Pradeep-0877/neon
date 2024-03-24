pipeline{
    agent any
    environment{
        NAME='pradeep'
    }
    stages{
        stage('Build'){
            environment{
                NAME = 'Ravi'
                comment = "This is specific to only a stage only and not global"
            }
            steps{
                 echo "hello $NAME"
                 echo "$comment"
                 echo "printenv"
            }
        }
    }
}
