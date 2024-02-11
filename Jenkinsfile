pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf grafana'
                sh 'git clone https://github.com/sanjay0288/grafana.git'
            }
        }
        stage('Deploy Grafana') {
            steps {
                sh 'sudo ansible-playbook grafana.yml -vvv -i inventory/hosts'
            }
        }
    }
}
