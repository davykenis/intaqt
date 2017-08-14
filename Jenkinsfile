pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Build completed'
      }
    }
    stage('Run sanity Test') {
      steps {
        parallel(
          "Run sanity Test": {
            echo 'Sanity Test'
            
          },
          "Run Functional Test": {
            echo 'Functional Tests are running'
            
          },
          "Run Regression Test": {
            echo 'Regression Tests did run'
            
          }
        )
      }
    }
    stage('Create Report') {
      steps {
        echo 'Report is created'
      }
    }
    stage('Send report') {
      steps {
        echo 'Report is send'
      }
    }
  }
}