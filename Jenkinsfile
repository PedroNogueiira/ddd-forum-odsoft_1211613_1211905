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
                // If you want to clean up files, uncomment or add appropriate steps
                // sh "npm run clean"
                sh 'npm prune'
                sh 'rm -rf node_modules'
            }
        }
    }
}
