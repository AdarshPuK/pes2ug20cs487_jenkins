pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'g++ main/hello.cpp'
        build 'PES2UG20CS262-1'
        echo 'Build Stage Successful'
      }
    }
    
    stage('Test') {
      steps {
        sh './a.out'
        echo 'Test Stage Successful'
       }
     }
    
    stage('Deploy') {
      steps {
        echo 'Deploy Stage Successful'
      }
    }
  }
  post {
    failure {
      echo 'Pipeline failed'
}
}
}
