pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/14vasudha/ansiblesetup.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh '''
                export ANSIBLE_HOST_KEY_CHECKING=False
                ansible-playbook -i /etc/ansible/hosts installwebservers.yml
                '''
            }
        }
    }
}
