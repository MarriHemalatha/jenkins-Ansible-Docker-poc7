
pipeline {
    agent any

    stages {

        stage('Clone Code') {
            steps {
                git 'https://github.com/MarriHemalatha/jenkins-Ansible-Docker-poc7'
            }
        }

        stage('Deploy using Ansible') {
            steps {
                sh 'ansible-playbook inventory.ini deploy.yml'
            }
        }
    }
}
