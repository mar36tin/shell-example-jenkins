pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh '''chmod +x ./testscript.sh
./testscript.sh > script.txt'''
      }
    }

  }
}