pipeline {
    agent any
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'apache-maven') {
                     bat 'mvn clean install'
                }
            }
        }


        }