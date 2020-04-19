#!/usr/bin/groovy

pipeline{
    agent any
    stages {
        stage('tag stage'){
            steps {
                gitTag()
            }
        }
    }
}

def gitTag(){
    String date = new Date().format('yyyyMMddhhmmss')
    String branch = "${env.GIT_BRANCH}"
    String tag = "v${date}-${branch}"
    tag = tag.replaceAll('/', '-')
    String message = "tagged via jenkins - ${tag}"
    print message

    bat "echo from bat before tag ${tag} after tag"
    bat "git tag -a ${tag} -m \"tagging with ${message}\""
	bat "git tag > tag_list"
	bat "git add tag_list"
	bat "git commit -m 'Pushing tag_list'"
	bat "git push"
	bat "git push origin ${tag}"
}