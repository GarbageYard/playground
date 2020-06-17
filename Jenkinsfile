pipeline {
	agent any

	stages {
		stage('Push') {
             steps {
                sh '''#!/bin/bash
					echo ${GIT_BRANCH}
					BRANCH=$(echo ${GIT_BRANCH} | cut -d "/" -f2)
					echo "Branch: ${BRANCH}"
                '''
            }
        }
	}
}