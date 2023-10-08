pipeline {
  agent any
    
    environment {
        SSH_CRED = credentials('SSH_CRED')
    }
    stages {
      stage {'performing dry run'} {
        steps { 
            sh '''
               env
               ansible-playbook robo-dryrun.yml  -e ENV=dev -e COMPONENT=mongodb -e ansible_user=${SSH_CRED_USR} -e ansible_password=${SSH_CRED_PSW} 
            
            '''
            } 
        }
    }
}