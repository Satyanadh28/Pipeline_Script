pipeline {
    agent none
    stages {
	
	stage('Non-Parallel Stage') {
	    agent {
                        label "master"
                }
        steps {
                echo 'This stage will be executed first'
                }
        }

	
        stage('Run Tests') {
            parallel {
                stage('Test On master') {
                    agent {
                        label "master"
                    }
                    steps {
						echo "Task1 on master"
					}
                }
            }
        }
    }
}
