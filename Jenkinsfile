pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        build(job: 'build test from git hello.c', propagate: true, quietPeriod: 1)
        echo 'Hello My pipeline'
      }
    }

  }
}