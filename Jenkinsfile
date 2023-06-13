def snapshotObj = ''
pipeline{
    agent any
    stages {
        stage('Pre'){
            steps {
                echo 'Pre exist'
                sleep 3
            }
        }
        stage('Upload'){
            steps{
                script{
                    snapshotObj=snDevOpsConfig(
                        applicationName:"AdoPublish Test",
                        configFile:"configOne.json",
                        namePath:"TestCompOne/new/key",
                        target:"component",
                        dataFormat:"json",
                        outputFormat:"xml",
                        markFailed:true
                      )
                    echo "Final Obj"
                    echo "${snapshotObj}"
                }
            }
        }
    }
    post{
        always{
            echo ">>>>>Displaying Test results"
            junit '**/*_${BUILD_NUMBER}.xml'
        }
    }
}
        
