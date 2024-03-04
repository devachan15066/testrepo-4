pipeline {
  agent {
    kubernetes {
      yamlFile 'podtemplate.yaml'
    }
  }
  stages {
    stage('Build') {
      steps {
        withCredentials([azureServicePrincipal(credentialsId: '23-02-service-principal', variable: 'AZURE_CREDENTIALS')]) {
          script {
            // Access the credentials using the environment variable 'AZURE_CREDENTIALS'
            sh '''
            # Example usage:
            echo "Extracting client ID from credentials: $AZURE_CREDENTIALS.clientId"
            '''
          }
        }
      }
    }
  }
}
