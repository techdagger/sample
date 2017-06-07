pipeline {
  agent any
  stages {
    stage('dev') {
      steps {
        parallel(
          "dev": {
            echo 'this is dev stage'
            
          },
          "fix": {
            echo 'hi'
            
          }
        )
      }
    }
    stage('deploy') {
      steps {
        parallel(
          "deploy": {
            echo 'test'
            
          },
          "build": {
            echo 'build'
            
          }
        )
      }
    }
    stage('sanity') {
      steps {
        echo 'sanity'
      }
    }
    stage('regression') {
      steps {
        timestamps() {
          echo 'testing cases'
        }
        
      }
    }
    stage('Alm update') {
      steps {
        echo 'alm test case upade'
      }
    }
    stage('Log defects') {
      steps {
        echo 'log the defects'
      }
    }
  }
}