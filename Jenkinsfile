pipeline{
		agent any
		
		stages {
			stage ('compile stage') {
			
				steps {
					echo 'compile'
					withMaven(maven : 'maven_3_6_3){
					   sh 'mvn clean compile'
					}
				}
			}
			
			
			stage ('testing stage') {
				steps {
					echo 'run'
				}
			}
			
			
			stage ('deploy stage') {
				steps {
					echo 'deploy'
					}
			}
		}

}