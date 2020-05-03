pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(region:'us-east-2',credentials:'aws-static'){
            sh 'echo "Uploading the file"'
            s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, bucket: 'luisperez-jenkinspractice-nanodegree', file: 'index.html')
        }
      }
    }

  }
}