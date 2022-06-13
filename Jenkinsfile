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
          rem Testing docker in jenkins
          echo %CD%
          docker image ls
          docker ps
          docker stop sample-app-01
          docker rm -f sample-app-01
          docker run -dp 3000:3000 --name sample-app-01 getting-started
        '''
      }
    }
  }
}
