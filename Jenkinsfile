pipeline{
    agent any
    environment{ //now we are defining environment in pipeline scope this variables is available for all stages
       name='pradeep'

       course='GCP'

    }
    stages{
        stage('Build'){
            steps{
                echo "eslcome ${name}"
                echo "you enrolled in ${gcp} course"

            }
        }
        stage('Testing'){
            environment{ //this environment is scoped to only stage level
                cloud='GCP'

            }
            steps{
                echo "You are certified in ${cloud}" //note thet ${} only works with double quotes
            }
        }
    }
}
