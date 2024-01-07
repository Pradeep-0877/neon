pipeline{
    agent any
    stages{
        stage("Build"){
            steps{
                timeout {time: 300, unit: 'SECONDS'}
                input message: "Are you sure ,Building this appliccation", ok: 'yes', submitter: 'pradeep Reddy'
                scho 'Building my application'
            }
        }
        stage('B'){
            steps{
                echo "executing multi branch pipeline"
                echo 'it is a on different branch'
            }
        }
    }
}
