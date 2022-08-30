
pipeline {
    options {
        timestamps ()
    }
    agent any

    stages {
        stage('stage:[1]') {
            steps('steps:[1]') {
                withCredentials([string(credentialsId: 'create_user_john', usernameVariable: 'USERNAME', passwordVariable: 'PASSWORD')]) {
                    sh ''' ansible-playbook -i host.ini playbook.yaml'''
                }
            }
        }
    }
}
