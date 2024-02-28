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
            withCredentials([azureServicePrincipal(credentialsId: 'supportjenkins', variable: 'AZURE_CREDENTIALS')])
            echo "TESTING AGENT"
        }
      }
    }
  }
}
