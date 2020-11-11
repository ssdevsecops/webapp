pipeline {
    agent any

    
    stages {
        stage('ansiblerun') {
            steps {
                // Run Maven on a Unix agent.
                sh "ansible-playbook apply_role.yml"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }
    }
}