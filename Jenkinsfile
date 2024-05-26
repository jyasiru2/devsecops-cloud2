pipeline {
  agent any

  stages {

    stage('git version') {
      steps {
        sh "git version"
      }
    }

    stage('maven version') {
      steps {
        sh "mvn -version"
      }
    }

    stage('docker version') {
      steps {
        sh "docker -v"
      }
    }

    stage('kubernetes version') {
      steps {
        withKubeConfig([credentialsId: 'kubeconfig']) {
          sh "kubectl version --short"
        }
      }
    }
  }
}