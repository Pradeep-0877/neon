pipeline{
    agent any
    stages{
        stage("Deploying..."){
            when{
                    branch 'hotfix'
                }
            steps{
                
                
                    timeout(time: 10,unit: 'SECONDS'){
                        input message: 'Are you building the application ?',ok: 'yes',submitter: 'ullas'  
                    
                }
            }
        }
    }
}
