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
          rem docker run -dp 3000:3000 getting-started
          echo %CD%
          docker image ls
          docker ps
          docker stop dc4691f373f2
        '''
      }
    }
  }
}
