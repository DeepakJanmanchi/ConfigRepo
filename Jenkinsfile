def changeset = ''
pipeline{
    agent any
    stages {
        stage('Register'){
            steps{
                sleep 3
            }
        }
        stage('Upload'){
            steps{
                script{
                    changeset = snDevOpsConfig(applicationName:"TrialApp",configFile:"Config/*.json",namePath:"TestCompOne/new/multiFile",target:"deployable",deployableName:"Development_1",autoCommit:"true",autoValidate:"true",autoPublish:"true")
                }
                echo "${changeset}"
            }
        }
    }
}
        
