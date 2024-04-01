pipeline {
    agent any
    
    stages{
        stage("Code"){
            steps{
                git url: "https://github.com/LondheShubham153/two-tier-flask-app.git", branch: "jenkins"
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