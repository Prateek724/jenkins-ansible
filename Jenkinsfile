pipeline {

agent any

stages{

stage('Checkout'){
 steps{
      git branch: 'main', credentialsId: 'Git_Credentails', url: 'https://github.com/Prateek724/jenkins-ansible.git'
      }
}
stage('AnsibleExecution'){
 steps{
    ansiblePlaybook credentialsId: 'auser', disableHostKeyChecking: true, installation: 'ansible', inventory: 'dhost.inv', playbook: 'apache.yml', vaultTmpPath: ''
     }
   }
}
}
