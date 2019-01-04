pipeline {
		agent any
		stages {   

					stage ( 'Chicken into GitHub' ) {								
							steps {
										git credentialsId: '0718e330-6d54-4bde-ae21-0402451752d3', url: 'https://github.com/venkeystore/Maven_Project.git'
									}	
						}		
		
					stage ( 'Clean Phase' ) {								
							steps {
									withMaven (maven : 'M2_HOME_3.5' ) {
										sh 'mvn clean '
											}
								}	
						}

					stage ( 'Compalation Phase' ) {
							steps {
									withMaven (maven : 'M2_HOME_3.5' ) {
										sh 'mvn compile'
											}
								}	
						}					
					stage ( 'Test Phase' ) {
							steps {
									withMaven (maven : 'M2_HOME_3.5' ) {
										sh 'mvn test'
											}
								}	
						}
						
					stage ( 'Results' ) {
							junit '**/target/surefire-reports/TEST-*.xml'
							archive 'target/*.jar'
						}
					
					stage ( 'Package' ) {
							steps {
									withMaven (maven : 'M2_HOME_3.5' ) {
										sh 'mvn clean package'
											}
								}	
						}						
					stage ( 'Code Coverage' ) {
							steps {
										jacoco()
								}		
						}

						
					}
			}