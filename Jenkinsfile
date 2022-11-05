pipeline {
    agent none
    stages {
	
	stage('Non-Parallel Stage') {
	    agent {
                        label "Built-In Node"
                }
        steps {
                echo 'This stage will be executed first'
                }
        }

	
        stage('Run Tests') {
            parallel {
                stage('Test On Built-In Node') {
                    agent {
                        label "Built-In Node"
                    }
                    steps {
						echo "Task1 on Built-In Node"
					}
                }
            }
        }
    }
}
