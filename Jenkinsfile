pipeline {
    agent any

    
    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url:'https://github.com/ssdevsecops/webapp.git'

                // Run Maven on a Unix agent.
                sh "ansible-playbook apply_role.yml"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }
    }
}