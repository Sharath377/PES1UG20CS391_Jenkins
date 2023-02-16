pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ -o PES1UG20CS391-1 PES1UG20CS391.cpp'
      }
    }
    stage('Test') {
      steps {
        sh './PES1UG20CS391-'
      }
    }
    stage('Deploy') {
      steps {
        sh 'echo "Deployment Step"'
      }
    }
  }
  post {
    always {
      echo 'Pipeline completed'
    }
    failure {
      echo 'Pipeline failed'
    }
  }
}
