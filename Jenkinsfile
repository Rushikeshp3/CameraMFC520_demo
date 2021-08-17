pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}




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



/*
stage: test
  script:
    - gtest.exe --gtest_output="xml:report.xml"
  artifacts:
    when: always
    reports:
      junit: report.xml
*/
