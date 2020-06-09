pipeline {
	agent any

	environment {
		git_commit_msg = sh(returnStdout: true, script: 'git log --format="medium" -1 c8b040d | tail -1').trim()
    }

	stages {
		stage ('Speak') {
			when {
				// Use 'git_commit_msg' here to check the string you're interested in
				expression { git_commit_msg =~ /[cd:deploy]/ }
			}
			steps {
				echo "Hello, there!"
			}
		}
	}
}