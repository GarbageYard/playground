pipeline {
	//agent { label 'slave1' }
	agent any
	
	stages {
		stage('unzip') {
            steps {
                //unzip dir: 'C:\\package', glob: '', zipFile: 'test.zip'
                unzip zipFile: 'test.zip', dir: 'C:\\package', glob: ''
            }
        }
	}
}