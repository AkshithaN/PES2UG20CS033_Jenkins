pipeline {
    agent any

stages{
  stage('Build') {
    steps{
      sh 'g++ -o PES2UG20CS033 PES2UG20CS033.cpp'
       build job: 'PES2UG20CS033-1'
    }
  }

  stage('Test') {
    steps{
       sh './PES2UG20CS033'
        
    }
  }

  stage('Deploy') {
    steps{
      echo 'DEPLOYMENT SUCCESSFUL'
    }
  }
}
post {
    failure {
        echo 'Pipeline Failed'
    }
  }
}

