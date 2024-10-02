pipeline {
    agent any
    stages {
        stage("Checkout") {
            steps {
                checkout scm
            }
        }

        stage("Install dependencies") {
            steps {
                sh "npm install"
            }
        }

        stage("Run tests") {
            steps {
                sh "npm test"
            }
        }

        stage("Build") {
            steps {
                sh "npm run-script build"
            }
        }

        stage("Deploy") {
            steps {
                sh "npm run deploy"
            }
        }

        stage("Clean") {
            steps {
                // Uncomment or add your cleanup command here
                // sh "npm run clean"
            }
        }
    }
}
