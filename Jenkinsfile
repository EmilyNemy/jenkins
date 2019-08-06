pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
	stage('Input step') {
	    steps {
	        timeout(time: 1, unit: "MINUTES") {
                input message: 'Approve Deploy?', ok: 'Yes'
                }
	    }
	}
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}

