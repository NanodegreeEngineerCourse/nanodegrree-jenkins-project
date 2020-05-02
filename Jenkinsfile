pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                s3Upload(bucket:'luisperez-jenkinspractice-nanodegree',file:'index.html')
            }
        }
    }
}