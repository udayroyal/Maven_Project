pipeline {
		agent any
		stages {
				stage ('Clean Stage') {
						steps {
								withMaven (maven : '/root/.jenkins/workspace/Pipeline as a code') {
									sh 'mvn clean'
										}
							}	
					}
					
					
					
				stage ('Copilation') {
						steps {
								withMaven (maven : '/root/.jenkins/workspace/Pipeline as a code') {
									sh 'mvn compile'
										}
							}		
					}
					
				stage ('Unit Test') {
						steps {
								withMaven (maven : '/root/.jenkins/workspace/Pipeline as a code') {
									sh 'mvn test'
										}
							}		
					}
					
				stage ('Packaging') {
						steps {
								withMaven (maven : '/root/.jenkins/workspace/Pipeline as a code') {
									sh 'mvn package'
										}
							}		
					}
				}
			}