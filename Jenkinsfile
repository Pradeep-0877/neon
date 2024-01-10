pipeline{
    agent any
    stages{
        stage("deploying to dev ENV"){
            steps{
                echo "Successfully deployed to dev"
            }
        }
        stage("Deploy to prod"){
            options{
                timeout(time: 300, unit: "SECONDS")
                 buildDiscarder(logRotator(numToKeepStr: '2')) 
            }
            input{
                message "Approve"
                ok "approved"
                submitter "ravi"
                submitterParameter "whoApproved"
                parameters{
                    string(name: "CHANGE_TICKET", defaultValue: "CH!12345", description: "provide the change ticket number")
                    booleanParam(name: "SRE Approved??", defaultValue: false, description: "Are you sure SRE approved")
                    choice(name: "DEPLOY_ENV", choices: "release\nnormal", description: "Mention the ploy environment")
                    text(name: "RELEASE_NOTES", description: "Provide the release notes here")
                    password(name: "PASSWORD", defaultValue: "Pradeep@0877", description: "provide your original password")
                    credentials(name: "myCredentials", description: "Provide your credentials here", required: true)

                }
            }
            steps{
                    echo "The Ticket name is ${CHANGE_TICKET}"
                    echo "The is approved by ${whoApproved}"
                    echo "This is a ${DEPLOY_ENV} environment"
                    echo "the release notes is ${RELEASE_NOTES}"
                }
        }
    }
}
