// Run on an agent where we want to use Go
pipeline{
    agent any
    environment{
        root= "/usr/local/go/bin/go"
        scmUrl='https://github.com/hprks/sample-go-jenkins.git'
    }
    stages{
        stage("Git Clone"){
            steps{
                git url: "${scmUrl}"
            }
        }
        stage("Dockerize"){
            steps{
                sh "docker build -t sample-go-jenkins ."
            }
        }
        stage("Deploy"){
            steps{
                 echo "DEPLOY SUCCESS"       
            }
        }                        
    }
}