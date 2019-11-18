pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(jdk: 'jdk11.0.5', maven: 'mvn3.5.2') {
                    sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(jdk: 'jdk11.0.5', maven: 'mvn3.5.2') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(jdk: 'jdk11.0.5', maven: 'mvn3.5.2') {
                    sh 'mvn install'
                }
            }
        }
    }
}
