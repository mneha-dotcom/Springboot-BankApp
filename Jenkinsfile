pipeline{
    agent any;
    stages{
        stage("code"){
            steps {
                git url: "https://github.com/mneha-dotcom/Springboot-BankApp.git", branch:"prd"
            }
        }
        stage("build"){
            steps {
                sh "docker build -t app ."
            }
        }
        stage("deploy"){
            steps {
                sh "docker compose down && docker compose up -d"
            }
        }
    }
}
