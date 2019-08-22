pipeline {
	//agent { label 'slave1' }
	agent any
	
	triggers {
		pollSCM '* * * * *'
	}

	stages {
		stage ('Echo') {
			steps {
				echo 'Hello, World!!!!!'
			}
		}
	}
}