/* pipeline {
    agent any 
    stages {
                  stage('Build') { 
                                 steps {
                                             sh 'make'
                                         }   
                                  }
                   stage('Test') { 
                                 steps {
                                          sh 'make check'
                                             xunit 'report/**/*.xml'   
                                   //      }
                /*                    }
                  stage('Deploy') { 
                                    steps {
                                            sh 'make publish'
                                             }
                                    }
             }
}
*/




stage: test
  script:
    - gtest.exe --gtest_output="xml:report.xml"
  artifacts:
    when: always
    reports:
      junit: report.xml
