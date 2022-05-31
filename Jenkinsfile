#!/usr/bin/env groovy
pipeline {
  agent any
  
  stages {
    stage("build") {
      steps {
        bat '''
          docker build -t hello_there .
        '''
      }
    }
    stage("run") {
      steps {
        sh '''
          docker run --rm hello_there
        '''
      }
    }
  }
}
