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
                                withMaven(maven : 'apache-maven') {
                                    bat 'mvn test'
                                }
                            }
                        }

			}
		}