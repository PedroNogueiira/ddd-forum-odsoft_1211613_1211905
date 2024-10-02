pipeline {
    agent any 
    stages{
        stage("Checkout"){
            steps{
                checkout scm
             }
     }

        stage("install dependencies"){
            steps{
                sh "npm install"
            }
        }

        stage("Run tests"){
            steps{
                sh "npm test"
            }
        }

        stage("Build"){
            steps{
                sh "npm run-script build"
            }
        }

        stage("Deploy"){
            steps{
                sh "npm run deploy"
            }
        }

        stage("Clean"){
            steps{
              //  sh "npm run clean"
            }
        }

        
    }
}
