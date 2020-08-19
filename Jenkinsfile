pipeline{
    agent any
    stages{
        stage('SCM checkout'){
            steps{
                git 'https://github.com/ChetanKumar07/myapp-ansible'
            }
        }
        stage('Execute Ansible Playbook'){
            steps{
                ansiblePlaybook credentialsId: 'Ansible_Private_Key', disableHostKeyChecking: true, installation: 'Ansible_Test', inventory: 'dev.inv', playbook: 'apache.yml'
            }
        }
    }
}
