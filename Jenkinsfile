pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
          withAWS(credentials:'jenkins') {
            s3Upload(bucket: 'luisperez-jenkinspractice-nanodegree', file: 'index.html')
          }
      }
    }

  }
}