pipeline {
  agent {
    kubernetes {
      yamlFile 'podtemplate.yaml'
      azureCredentialsId 'supportjenkins' 
    }
  }
  stages {
    stage('Build') {
      steps {
        script {
          echo "TESTING AGENT"
          // Add your build steps here
        }
      }
    }
  }
}
