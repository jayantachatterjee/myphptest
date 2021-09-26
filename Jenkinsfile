pipeline {
	agent any
	stages {
		stage('Build Stage') {
			steps {
				git 'https://github.com/jayantachatterjee/myphptest.git'
			}
		}
		stage('Deploy Stage') {
			steps {
				sh 'rsync -avzhr /var/lib/jenkins/workspace/php-pipeline ansible@172.31.47.154:/home/ansible/php-project'
			}
		}
	}
}
