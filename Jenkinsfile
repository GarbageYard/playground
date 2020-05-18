pipeline {
	//agent { label 'slave1' }
	agent any
	
	stages {
		stage('unzip') {
            steps {
                script {
					unzip dir: 'E:\\package', glob: '', zipFile: 'test.zip'
                }
            }
        }
	}
}