pipeline {
  environment {
    registry = '540451631109.dkr.ecr.us-east-1.amazonaws.com/jenkins-ecr-cicd'
    registryCredential = 'aws-ecr-credentials'
    dockerImage = ''
  }
  agent any
  stages {
   stage('Create ECR repository') {
      steps {
            withAWS(credentials: 'aws-ecr-credentials', region: 'us-east-1') {
                  sh "chmod +x ./create_repo.sh"
                  sh "./create_repo.sh"
                }
            }
       }
 
    }
   
}
