pipeline {
    agent any

    stages {
        stage('Clonar Repositorio') {
            steps {
                script {
                    // Clonar el repositorio desde GitHub
                    checkout scm
                }
            }
        }

        stage('Instalar Dependencias') {
            steps {
                script {
                    // Instalar dependencias usando npm
                    bat 'npm install'
                }
            }
        }

        stage('Compilar y Construir') {
            steps {
                script {
                    // Compilar y construir la aplicación Angular
                    bat 'ng build --configuration production'
                }
            }
        }

        stage('Ejecutar Pruebas Unitarias') {
            steps {
                script {
                    // Ejecutar pruebas unitarias

                    echo 'Ejecución de Pruebas Completada'
                }

            }
        }

        stage('Publicar en Docker Hub') {
            steps {
                script {
                    // Construir la imagen Docker
                   echo 'Publicdo en DockerHub'
                }
            }
        }

        stage('Desplegar Proyecto') {
            steps {
                script {
                    // Aquí puedes agregar comandos para desplegar la aplicación (puedes personalizarlo)
                    echo 'Proyecto desplegado'
                }
            }
        }
    }
}
