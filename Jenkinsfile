@Library('Shared')_
pipeline{
    agent { label 'avinash'}
    
    stages{
        stage("Code clone"){
            steps{
                sh "whoami"
            clone("https://github.com/avinash01123/note-apps.git","master")
            }
        }
        stage("Code Build"){
            steps{
            dockerbuild("note-app","latest")
            }
        }
        stage("Push to DockerHub"){
            steps{
                dockerpush("dockerHubCreds","note-app","latest")
            }
        }
        stage("Deploy"){
            steps{
                deploy()
            }
        }
        
    }
}
