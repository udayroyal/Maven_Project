pipeline {
		agent any
		stages {
				stage ('Clean Stage') {
						steps {
								withMaven (maven : 'MAVEN_3.5/bin') {
									sh 'mvn clean'
										}
							}	
					}
					
					
					
				stage ('Copilation') {
						steps {
								withMaven (maven : 'MAVEN_3.5/bin') {
									sh 'mvn compile'
										}
							}		
					}
					
				stage ('Unit Test') {
						steps {
								withMaven (maven : 'MAVEN_3.5/bin') {
									sh 'mvn test'
										}
							}		
					}
					
				stage ('Packaging') {
						steps {
								withMaven (maven : 'MAVEN_3.5/bin') {
									sh 'mvn package'
										}
							}		
					}
				}
			}