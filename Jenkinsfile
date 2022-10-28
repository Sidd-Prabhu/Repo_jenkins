pipeline {
  agent any
  options {
    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
  }
  stages {

    stage('Java version') {
      steps {
        sh 'java -version'
      }
    }

    stage('Readme') {
      when {
        branch "newBranch-*"
      }
      steps {
        sh "cat README.md"
      }
      
    }
  }
}
