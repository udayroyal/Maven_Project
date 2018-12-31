pipeline {
		agent any
		stages {
				stage ( 'Clean Stage' ) {
						steps {
								withMaven (maven : 'M2_HOME_3.5' ) {
									sh 'mvn clean'
										}
							}	
					}
					
					
					
				stage ( 'Copilation' ) {
						steps {
								withMaven (maven : 'M2_HOME_3.5' ) {
									sh 'mvn compile'
										}
							}		
					}
					
				stage ( 'Unit Test' ) {
						steps {
								withMaven (maven : 'M2_HOME_3.5' ) {
									sh 'mvn test'
										}
							}		
					}
					
				stage ( 'Packaging' ) {
						steps {
								withMaven (maven : 'M2_HOME_3.5' ) {
									sh 'mvn package'
										}
							}		
					}
				}
			}