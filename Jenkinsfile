pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/your/repo.git'
            }
        }
        stage('Deploy Grafana') {
            steps {
                sh 'ansible-playbook deploy-grafana.yml -i inventory/hosts'
            }
        }
    }
}
