pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                echo 'Obteniendo el código del repositorio...'
            }
        }
        stage('Test') {
            steps {
                script {
                    def file = 'index.html'
                    if (fileExists(file)) {
                        echo "¡Prueba exitosa! El archivo ${file} existe."
                    } else {
                        error "¡Prueba fallida! El archivo ${file} no se encontró."
                    }
                }
            }
        }
        stage('Deploy to S3') {
            steps {
                echo 'Desplegando el archivo a AWS S3...'
                // Aquí iría la lógica para subir el archivo a AWS. La agregaremos después.
            }
        }
    }
}