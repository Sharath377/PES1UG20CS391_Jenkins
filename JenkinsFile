pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES1UG20CS391-1 PES1UG20CS391-1.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './PES1UG20CS391-1'
            }
        }
        stage('Deploy') {
            steps {
                sh 'make deploy'
            }
        }
    }
    post {
        always {
            sh 'rm -f PES1UG20CS391-1'
        }
        failure {
            echo 'pipeline failed'
        }
    }
}
