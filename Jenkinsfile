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
                bat "npm install"
            }
        }

        stage("Run tests") {
            steps {
                bat "npm test"
            }
        }

        stage("Build") {
            steps {
                bat "npm run build"
            }
        }

        stage("Deploy") {
            steps {
               // bat "npm run deploy"
            }
        }

        // Clean stage should be placed in the same format as others
        stage("Clean") {
            steps {
                bat 'npm prune'
                bat 'rmdir /s /q node_modules'
            }
        }
    }
}
