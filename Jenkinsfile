#!/usr/bin/env groovy
pipeline {
  agent any

  stages {
    stage("build") {
      steps {
        bat '''
          docker --version
        '''
      }
    }
    stage("run") {
      steps {
        bat '''
          docker run -dp 3000:3000 getting-started
        '''
      }
    }
  }
}
