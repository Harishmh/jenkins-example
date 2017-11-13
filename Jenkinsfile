pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(maven : 'MAVEN_HOME') {
                    bat 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'MAVEN_HOME') {
                    bat 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
          //  steps {
            //    withMaven(maven : 'MAVEN_HOME') {
            //        bat 'mvn deploy'
                //}
            bat xcopy C:\Program Files (x86)\Jenkins1\workspace\jenkins_pipeline\target\ C:\Dev_Harish\ \s
           // }
        }
    }
}
