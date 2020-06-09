pipeline {
	agent any

	environment {
		git_commit_msg = sh(returnStdout: true, script: 'git log --format="medium" -1 ${GIT_COMMIT} | <fetch-commit-message>').trim()
    }

	stages {
		stage ('Speak') {
			when {
				// Use 'git_commit_msg' here to check the string you're interested in
				expression { params.REQUESTED_ACTION == 'greeting' }
			}
			steps {
				echo "Hello, bitwiseman!"
			}
		}
	}
}