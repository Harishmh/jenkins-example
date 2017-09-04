pipeline {
    agent any
	stages {
        stage ('Compile Stage') {
			steps {
				withMaven(maven : 'apache-maven') {
                     bat 'mvn clean compile'
					 }
					}
				}
				stage ('Testing Stage') {


                                steps {
                                                /* `make check` returns non-zero on test failures,
                                                * using `true` to allow the Pipeline to continue nonetheless
                                                */
                                                sh 'make check || true'
                                                junit '**/target/*.xml'
                                            }

                        }
                 stage ('Deployment2 Stage') {
                                             steps {
                                                 withMaven(maven : 'apache-maven ') {
                                                     bat 'mvn deploy'
                                                 }
                                             }
                                         }
			}
		}