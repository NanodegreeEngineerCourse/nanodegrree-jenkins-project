pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        sh 'echo "hola"'
        s3Upload(bucket: 'luisperez-jenkinspractice-nanodegree', file: 'index.html')
      }
    }

  }
}