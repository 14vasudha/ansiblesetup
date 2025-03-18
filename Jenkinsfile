pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/ansiblesetup.git' 
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh '''
                ansible-playbook -i hosts.ini install_apache.yaml
                '''
            }
        }
    }
}
