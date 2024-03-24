pipeline{
    agent any
    environment{
        NAME='pradeep'
    }
    stages{
        stage('Build'){
            environment{
                comment = "This is specific to only a stage only and not global"
            }
            steps{
                 echo "hello $NAME"
                 echo "$comment"
            }
        }
    }
}
