pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf prometheus'
                sh 'git clone https://github.com/gshashi1408/prometheus.git'
            }
        }
        stage('Deploy Prometheus') {
            steps {
                sh 'sudo ansible-playbook prometheus.yml -i inventory/hosts'
            }
        }
    }
}
