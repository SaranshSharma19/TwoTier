pipeline {
    agent any
    
    stages{
        stage("Code"){
            steps{
                git url: "https://github.com/SaranshSharma19/TwoTier", branch: "main"
            }
        }
        stage("Build & Test"){
            steps{
                sh "docker build . -t flaskapp"
            }
        }
        stage("Deploy"){
            steps{
                sh "docker-compose down && docker-compose up -d"
            }
        }
    }
}
