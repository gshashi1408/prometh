pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                sh 'rm -rf prometh'
                sh 'git clone https://github.com/gshashi1408/prometh.git'
            }
        }
        stage('Deploy Prometheus') {
            steps {
                sh 'ansible-playbook prometheus.yml -i inventory/hosts'
            }
        }
    }
}
