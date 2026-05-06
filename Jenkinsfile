pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git 'https://github.com/MarriHemalatha/jenkins-Ansible-Docker-poc7'
            }
        }

        stage('Build Image') {
            steps {
                sh 'docker build -t myapp .'
            }
        }

        stage('Run Container') {
            steps {
                sh '''
                docker rm -f myapp || true
                docker run -d -p 80:80 --name myapp myapp
                '''
            }
        }
    }
}
