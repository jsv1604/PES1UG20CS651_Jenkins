pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o output_file task5.cpp'
                build job : 'PES1UG20CS651-1'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                sh './out'
              echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deployment Successful'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
