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
                    changeset = snDevOpsConfigUpload(applicationName:"TrialApp",deployableName:"Development_1", "autoCommit": true, "autoDelete":"",  "autoPublish": true, "autoValidate": true, target:"deployable",namePath:"test/NoIMpact",configFile:"config.json",dataFormat:"json")
                }
                echo "${changeset}"
            }
        }
    }
}
        
// def changeset = ''
// pipeline{
//     agent any
//     stages {
//         stage('Register'){
//             steps{
//                 sleep 3
//             }
//         }
//         stage('Upload'){
//             steps{
//                 script{
//                     changeset = snDevOpsConfig(applicationName:"TrialApp",deployableName:"Development_1",isValidated:true,continueWithLatest:true,target:"deployable","autoDelete":"true",namePath:"test/NoIMpact",configFile:"*.json",dataFormat:"json")
//                 }
//                 echo "${changeset}"
//             }
//         }
//     }
// }
