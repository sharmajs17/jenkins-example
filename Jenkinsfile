pipeline {
    agent any

    stages {
         stage ('Build Stage') {

            steps {
                withMaven(maven : 'maven_3.5.0') {
                    sh 'mvn install'
                }
            }
        }

        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3.5.0') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3.5.0') {
                    sh 'mvn test'
                }
            }
        }


  //      stage ('Deployment Stage') {
  //          steps {
  //              withMaven(maven : 'maven_3.5.0') {
  //                  sh 'mvn deploy'
  //              }
  //          }
  //      }
    }
}
