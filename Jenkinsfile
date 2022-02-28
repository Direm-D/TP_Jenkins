pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        bat 'git --version'
        bat 'gradle --stop'
        bat 'gradle clean'
        bat 'gradle build'
      }
    }

  }
}