def changeset = ''
pipeline{
    agent any
    stages {
        stage('Upload'){
            steps{
                script{
                    changeset=snDevOpsConfigPipeline(
                        applicationName:"AdoPublish Test",
                        configFile:"configOne.json",
                        namePath:"TestCollOne/new/key",
                        collectionName:"TestCollTwo"
                        target:"collection",
                        autoCommit:true,
                        autoValidate:true,
                        dataFormat:"json",
                        exporterName:"returnAllData-now",
                        exporterFormat:"json",
                        fileName:""
                      )
                }
            }
        }
        stage('Register') {
             steps{
                 script {
                      snDevOpsConfigRegisterPipeline(changesetNumber:"${changeset}",applicationName:"AdoPublish Test")
                 }
             }
        }          
    }
}
        
