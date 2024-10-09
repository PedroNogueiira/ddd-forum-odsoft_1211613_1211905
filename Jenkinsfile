pipeline {
    agent any

//     environment {
//         NODE_VERSION = '12.22.12' // Ensuring the correct Node.js version
//     }
//
//     tools {
//         nodejs 'NodeJS 12.22.12'
//     }

    stages {
//         stage('Checkout') {
//             steps {
//                 // Checkout the 'pedro' branch from the repository
//                 git branch: 'pedro', url: 'https://github.com/PedroNogueiira/ddd-forum-odsoft_1211613_1211905.git'
//             }
//         }

        stage('Install Dependencies') {
            steps {
                script {
                    // Run Gradle task to install npm dependencies
                    ./gradlew.bat npm_install
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Run Gradle tasks to build the project
                    ./gradlew.bat npm_run_build
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run Gradle tasks to build the project
                    ./gradlew.bat npm_run_test
                }
            }
        }

        stage('Package') {
            steps {
                script {
                    // Run Gradle to Package the project into a .jar file
                    echo 'Packaging...'
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }

}