pipeline {
  agent any
  stages {
    stage('Lint HTML') {
      steps {
        sh 'tidy -q -e *.html'
      }
    }
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
