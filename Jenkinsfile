pipeline {
    agent any
    environment {
        ANSIBLE_CONFIG = "/etc/ansible/ansible.cfg"
    }
    stages {
        // Remove the manual 'clone Repo' stage entirely
        stage('Ansible Dry Run') {
            steps {
                sh 'ansible-playbook deploy.yml --check'
            }
        }
        stage('Ansible Apply') {
            steps {
                sh 'ansible-playbook deploy.yml'
            }
        }
    }
}
