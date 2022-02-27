pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh '''gradle build
gradle javadoc'''
        archiveArtifacts 'build/libs/*.jar, build/docs'
        junit 'build/test-results'
      }
    }

    stage('Mail Notification') {
      steps {
        mail(subject: 'TP Jenkins ', body: 'i\'m ur email', to: 'dalaldirem@gmail.com')
      }
    }

  }
}