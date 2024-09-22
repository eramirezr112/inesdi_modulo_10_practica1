pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Descargar el código del repositorio remoto
                git 'https://github.com/eramirezr112/inesdi_modulo_10_practica1.git'
            }
        }

        stage('Pruebas de SAST') {
            steps {
                // Simular ejecución de pruebas de calidad de código (SAST)
                echo 'Ejecución de pruebas de SAST'
            }
        }

        stage('Build') {
            steps {
                // Construir el contenedor Docker
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
