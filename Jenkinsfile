pipeline {
    agent any

    stages {

        stage('Clone Repo') {
            steps {
                git 'https://github.com/shahidafridi76/devops-cicd-demo.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t cicd-demo .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 80:80 cicd-demo'
            }
        }
    }
}
