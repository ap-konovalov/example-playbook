pipeline {
    agent any
    stages {
        stage('Clone from git') {
            steps {
                git 'https://github.com/ap-konovalov/example-playbook'
            }
        }
        stage('Run playbook') {
            steps {
                ansiblePlaybook(credentialsId: '7809a850-6110-4e3e-97ce-e9023bbd7be8', inventory: 'inventory/prod.yml', playbook: 'site.yml')
            }
        }
    }
}       
