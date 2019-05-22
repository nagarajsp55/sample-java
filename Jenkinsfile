pipeline {
    agent any
    stages {
        stage('One') {
                steps {
                        echo 'Hi, this is Prasanthi'
			
                }
        }
	    stage('Two'){
		    
		steps {
			input('Do you want to proceed?')
        }
	    }
        stage('Three') {
                when {
                        not {
                                branch "master"
                        }
                }
                steps {
			echo "Hello"
                        }
        }
        stage('Four') {
            steps {
                parallel("UnitTest": {
                    echo "UnitTesting is Running"
                },
                        "IntegrationTest": {
                            echo "Integration Tests are Running"
                        }
                )
            }
        }
        
                               
	}
}