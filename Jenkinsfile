pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'aws-static', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY']]) {
                    // some block
                    s3Upload(file:'index.html', bucket:'cali-jenkins-static', path:'./index.html')        

            }       
            }
        }
    }
}