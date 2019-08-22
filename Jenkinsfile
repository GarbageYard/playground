pipeline {
	agent { label 'slave1' }
	
	triggers {
		pollSCM '* * * * *'
	}

	stages {
		stage ('Echo') {
			steps {
				echo 'Hello, World!!!!'
			}
		}
	}
}