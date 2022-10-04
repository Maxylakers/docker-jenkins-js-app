pipeline {
    agent any
    stages {
        stage("run frontend") {
            steps {
				echo 'executing yarn..'
                nodejs('Node-10-17'){
                    sh 'yard install'
                }
             }
        }
	    stage("run backend") {
			steps {
				echo 'executing gradle...'
                withGradle(){
                    sh './gradlew -v'
                }
			}
		}
	}
}