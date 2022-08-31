
pipeline {
    options {
        timestamps ()
    }
    agent any

    stages {
        stage('stage:[1]') {
            steps('steps:[1]') {
                withCredentials([usernamePassword(credentialsId: 'create_user_johns', passwordVariable: 'PASSWORD', usernameVariable: 'USERNAME')]) {
                    sh ''' ansible-playbook -u vagrant -i host.ini -b playbook.yaml -e "passwordVariable=${PASSWORD}" -e "usernameVariable=${USERNAME}" '''
                }
            }
        }
    }
}
