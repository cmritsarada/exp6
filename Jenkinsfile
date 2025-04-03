pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                maven {
                    goals 'clean package'
                }
            }
        }
        stage('Deploy') {
            steps {
                sh "ansible-playbook -i /home/student/hosts.ini /opt/deployment.yml"
            }
        }
    }
}
