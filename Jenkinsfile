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
                 sh 'printenv'
            }
        }
        stage("Buils"){
            environment{
                tomcat_creds = credentials('tomcat')
            }
            steps{
                echo "The username is $tomcat_creds_usr"
                echo "The password is $tomcat_creds_psw"

            }

        }
    }
}
