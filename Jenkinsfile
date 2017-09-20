pipeline {
    agent any
	stages {
            stage ('Compile Stage') {
                steps {
                    withMaven(maven : 'apache-maven') {
                         sh 'mvn clean compile'
                         }
                        }
                    }
				stage ('Testing Stage') {

                    steps {
                        withMaven(maven : 'apache-maven') {
                        sh 'mvn test'
                            }
                        }
                    }


                 stage ('Deployment2 Stage') {
                                             steps {
                                                 withMaven(maven : 'apache-maven') {
                                                     sh 'mvn deploy'
                                                 }
                                             }
                                         }
			}
}