pipeline {
    agent any

       environment {                                // Pipeline Variables : All the stages of the pipeline can use it
       SSH_CRED = credentials('SSH_CRED')
    }
    stages {
        stage('performing a dry run'){
           steps {
             sh  '''
               env 
               ansible-playbook robo-dryrun.yml  -e ENV=dev -e COMPONENT=mongodb -e ansible_user=${SSH_CRED_USR} -e ansible_password=${SSH_CRED_PSW}
        
            '''
            }
         }
    }
}

