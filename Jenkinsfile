pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git url:'https://github.com/sibeshpatel9490/docker-jenkins-demo1.git', branch:'main'
            }
        }
        stage('Create Docker Image') {
            steps {
                bat 'docker build -t myimage .'
            }
        }
        stage('Create Container') {
            steps {
                bat 'docker run -d -p 8501:8501 myimage'
            }
        }
    }
}