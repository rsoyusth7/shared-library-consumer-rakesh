// Import the library by the name you gave it in Step 2
// The underscore (_) at the end is required! It loads everything.
@Library('shared-library-trainer') _ // use share library name here

pipeline {
    agent any

    stages {
        stage('Initialize') {
            steps {
                echo "Booting up..."
            }
        }

        stage('Compliance Check') {
            steps {
                // We are calling the file 'finTechAudit.groovy' as a function!
                helloWorld()
                script {
                    finTechAudit("Payment-Gateway-API at rakesh", "HIGH")
                }
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
            }
        }
    }
}