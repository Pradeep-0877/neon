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
    }
}
