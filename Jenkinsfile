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

            steps {
                withMaven(maven : 'Apache-maven') {
                    bat 'mvn test'
                }
            }
        }


        stage ('Deployment1 Stage') {
            steps {
                withMaven(maven : 'Apache-maven ') {
                    bat 'mvn deploy'
                }
            }
        }
    }
}