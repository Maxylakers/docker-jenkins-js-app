pipeline {
    agent any
    tools {
        gradle 'Gradle-6.2'
    }
    stages {
        stage("run frontend") {
            steps {
				echo 'executing yarn..'
                nodejs('Node-10-17'){
                    sh 'yarn install'
                }
             }
        }
	    stage("run backend") {
			steps {
				echo 'executing gradle...'
                    sh 'gradle --version'
			}
		}
	}
}