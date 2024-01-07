pipeline{
    agent any
    environment{ //now we are defining environment in pipeline scope this variables is available for all stages
       name='pradeep'
        git_creds=credentials('my_git_creds')

       course='GCP'

    }
    stages{
        stage('Build'){
            steps{
                echo "eslcome ${name}"
                echo "you enrolled in ${course} course"
                echo "my git creds are ${git_creds}"
                echo "my git username is ${GIT_CREDS_USR}" //if we want only usernam ewe will use _USR
                echo "my git password is ${GIT_CREDS_PSW}" //For getting my password we need to use _PSW after variable

            }
        }
        stage('Testing'){
            environment{ //this environment is scoped to only stage level
                cloud='GCP'
                name='habbeb'

            }
            steps{
                echo "You are certified in ${cloud}" //note thet ${} only works with double quotes
                echo "your name is ${name}"
                sh 'printenv'
            }
        }
        stage("deploy to prod"){
            when{
                // buildingTag=//
                //the Below expression we will be using  will accept only v1.2.2/1 and not accept v1.2.3
                tag pattern: "v\\d{1,2}.\\d{1,2}.\\d{1,2}"
            }
            steps{
                echo "deploying to production !!!!"
            }
        }
    }
}
