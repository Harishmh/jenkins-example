pipeline {
    agent any
	stages {
        stage ('Compile Stage') {
			steps {
				withMaven(maven : 'apache-maven') {
                     bat 'mvn clean install'
					 }
					}
				}
			}
		}