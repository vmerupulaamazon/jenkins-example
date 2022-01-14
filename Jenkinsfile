pipeline {
    agent any
    
     tools {
        maven 'Maven 3.8.4'
     }
    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'maven_3_8_4') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_8_4') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_8_4') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
