pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
          withAWS(credentials:'aws-static') {
            s3Upload(bucket: 'luisperez-jenkinspractice-nanodegree', file: 'index.html')
          }
      }
    }

  }
}
