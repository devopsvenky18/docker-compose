pipeline {
  
agent {
    
docker {
      image 'wordpress'
      args '-p 8000:80'
    }
  }
  
environment {
    CI = 'true'
  }
  
stages {
    
stage('Build') {
      
steps {
        sh 'npm install'
      }
    }
    
stage('Test') {
      
steps {
        sh './jenkins/scripts/test.sh'
      }
    }
  }
}
