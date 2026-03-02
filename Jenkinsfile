pipeline {
    agent any

    stages {
        stage('Fetch') {
            steps {
                echo 'Fetch from Repo.'
                git 'https://github.com/Adi222004/JavaRep.git'
            }
        }
        stage('Build') {
            steps {
                echo 'Building in Progress...'
                bat 'javac devops.java'
            }
        }
        stage('Execute') {
            steps {
                echo 'Execute the Program'
                bat 'java devops'
            }
        }
    }
    post{
        success{
            echo 'Pipeline built successfully'
        }
        failure{
            echo 'Pipeline is failed'
        }
    }
}
