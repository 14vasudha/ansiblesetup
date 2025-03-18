pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/14vasudha/ansiblesetup.git' 
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh '''
                ansible-playbook -i hosts.ini installwebservers.yml
                '''
            }
        }
    }
}
