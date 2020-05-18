pipeline {
	//agent { label 'slave1' }
	agent any
	
	stages {
		stage('unzip') {
            steps {
                unzip dir: 'C:\\package', glob: '', zipFile: 'test.zip'
            }
        }
	}
}