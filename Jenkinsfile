pipeline {
  agent any
  stages {
    stage('Upload to AWS') {
      steps {
        withAWS(credentials:'aws-static'){
            sh 'echo "Uploading the fileto the bucket"'
            s3Upload(pathStyleAccessEnabled: true, payloadSigningEnabled: true, bucket: 'luisperez-jenkinspractice-nanodegree', file: 'index.html')
        }
      }
    }

  }
}
