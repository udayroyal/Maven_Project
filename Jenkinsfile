pipeline {
		agent any
		stages {   

					stage ( 'Clone sources From GitHub' ) {								
							steps {
										git credentialsId: '0718e330-6d54-4bde-ae21-0402451752d3', url: 'https://github.com/venkeystore/Maven_Project.git'
									}	
						}		

		stage ( 'static code analysis is performed in the Stage ' ) {								
							steps {
									withMaven (maven : 'M2_HOME_3.5' ) {
										sh 'mvn sonar:sonar'
											}
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