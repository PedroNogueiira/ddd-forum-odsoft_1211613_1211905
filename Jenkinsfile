pipeline {
  agent { label 'master' }
  stages {
     stage("Create container") {
        steps {
        script {
           SEQ = sh(returnStdout: true, script: 'seq 1 9').trim()
           sh "echo '${SEQ}'"
           sh """
           for id in '{$SEQ}'
           do
              echo \$id
           done
           """
        }
        }
     }
  }
  }