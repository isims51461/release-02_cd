pipeline{
    agent any
    stages{
        stage('SCM Checkout'){
            steps{
                git 'https://github.com/isims51461/release-02_cd.git'
            }
        }
    
        stage('Run Ansible Playbook'){
            steps{
                ansiblePlaybook credentialsId: 'ansible_user_2', disableHostKeyChecking: true, installation: 'ansible', inventory: 'hosts', playbook: 'release-02.yml' 
            }
        }
        
    }
}
