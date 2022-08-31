
pipeline {
    options {
        timestamps ()
    }
    agent any

    stages {
        stage('stage:[1]') {
            steps('steps:[1]') {
                withCredentials([usernamePassword(credentialsId: 'create_user_johns', usernameVariable: USERNAME, passwordVariable: PASSWORD)]) {
                    sh ''' ansible-playbook -i host.ini playbook.yaml --extra-vars "ansible_sudo_pass=vagrant'''
                }
            }
        }
    }
}
