pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        git 'https://github.com/eramirezr112/inesdi_modulo_10_practica1.git'
      }
    }

    stage('Pruebas de SAST') {
      steps {
        echo 'Ejecución de pruebas de SAST'
      }
    }

    stage('Build') {
      steps {
        sh 'docker build -t devops_ws .'
      }
    }

  }
  post {
    success {
      echo 'Pipeline ejecutado correctamente'
    }

    failure {
      echo 'Error en la ejecución del pipeline'
    }

  }
}