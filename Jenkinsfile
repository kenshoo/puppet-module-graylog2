pipeline {
agent {label 'general-purpose-new'}
     stages {

            stage('ls') {
                steps {
                    checkout([$class: 'GitSCM', branches: [[name: 'master']],
                    extensions: [[$class: 'CleanCheckout'], [$class: 'RelativeTargetDirectory', relativeTargetDir: 'gradle-fpm-plugin']],
                    userRemoteConfigs: [[credentialsId: 'kenshoo-build-key', url: 'git@github.com:kenshoo/gradle-fpm-plugin']]]
                    )
		     echo 'Hello world!'
                     echo JENKINS_URL
                }
            }
	}
}
