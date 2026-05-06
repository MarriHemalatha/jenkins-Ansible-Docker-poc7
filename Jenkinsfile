pipeline {
    agent any

    stages {

        stage('Deploy using Ansible') {
            steps {
                sh 'ansible-playbook inventory.ini deploy.yml'
            }
        }
    }
}
