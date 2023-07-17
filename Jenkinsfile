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
                    changeset = snDevOpsConfigUpload(applicationName:"TrialApp",deployableName:"Development_1", "autoCommit": true, "autoPublish": true, "autoValidate": true, target:"deployable",namePath:"test/NoIMpact",configFile:"*.json",dataFormat:"json")
                }
                echo "${changeset}"
            }
        }
    }
}
        
