pipeline {
  agent {
    kubernetes {
      yamlFile 'podtemplate.yaml'
    }
  }
    stages {
      stage('Build') {
        steps {
          script {
            withCredentials([azureServicePrincipal(credentialsId: '23-02-service-principal', variable: 'AZURE_CREDENTIALS')])
            echo "TESTING AGENT"
        }
      }
    }
  }
}
