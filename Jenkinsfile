pipeline{
    agent any
    stages{
        stage("Deploy yo prod")[
            when{
                branch "release-*"
            }
            steps{
                echo "Deploying to $BRANCH_NAME"
            }
        ]
    }
}
