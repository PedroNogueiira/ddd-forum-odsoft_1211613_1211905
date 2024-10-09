pipeline {
    agent any

    stages {
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