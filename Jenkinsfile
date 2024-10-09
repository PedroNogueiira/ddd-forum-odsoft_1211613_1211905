pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from repo
                git 'https://github.com/PedroNogueiira/ddd-forum-odsoft_1211613_1211905.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Run Gradle task to install npm dependencies
                    sh './gradlew npm_install'
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Run Gradle tasks to build the project
                    sh './gradlew npm_run_build'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run Gradle tasks to build the project
                    sh './gradlew npm_run_test'
                }
            }
        }

        stage('Package') {
            steps {
                script {
                    // Run Gradle to Package the project into a .jar file

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