pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf grafana'
                sh 'git clone https://github.com/Nethravathi-R/grafana.git'
            }
        }
        stage('Deploy Grafana') {
            steps {
                sh 'sudo ansible-playbook grafana.yml -i inventory/hosts'
            }
        }
    }
}
