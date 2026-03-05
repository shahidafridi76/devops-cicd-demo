pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git branch: 'main', url: 'https://github.com/shahidafridi76/devops-cicd-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-demo .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker rm -f cicd-demo || true'
                sh 'docker run -d -p 8081:80 --name cicd-demo cicd-demo'
            }
        }

    }
}
