pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                withAWS(region:'af-south-1',credentials:'aws-static') {
                    // do something
                    
                }           
                s3Upload(file:'index.html', bucket:'cali-jenkins-static', path:'index.html')        
            }
        }
    }
}