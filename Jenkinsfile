pipeline {
    agent any
    triggers {
        pollSCM('* * * * *')
    }
    
    stages {
        stage('Ansible_Apply') {
            steps {
                sshagent(['ec2-user']) {
                    sh "ansible-playbook apply_role.yml"
 
                        }
                

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }
    }
}