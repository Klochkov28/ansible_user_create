pipeline {  
    agent any
     stages {
        step('start playbook') {
          withCredentials(
            [usernamePassword(credentialsId: 'create_user_john', 
                    usernameVariable: 'USERNAME', 
                    passwordVariable: 'PASSWORD')]) {
            sh 'ansible-playbook -i host.ini playbook.yaml'
            }
        }
      }
}
