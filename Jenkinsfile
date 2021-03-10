pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''chmod +x ./testscript.sh
./testscript.sh > script.txt'''
      }
    }

    stage('archive') {
      steps {
        archiveArtifacts(artifacts: '*.txt', fingerprint: true, onlyIfSuccessful: true)
      }
    }

    stage('finish') {
      steps {
        echo 'Completed'
      }
    }

  }
}