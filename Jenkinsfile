pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'Apache-maven') {
                     bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {sh
                withMaven(maven : 'Apache-maven') {
                    bat 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'Apache-maven ') {
                    bat 'mvn deploy'
                }
            }
        }
    }
}