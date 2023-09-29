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
                    bat 'ng test'
                }
                echo 'Ejecución de Pruebas Completada'
            }
        }

        // stage('Publicar en Docker Hub') {
        //     steps {
        //         script {
        //             // Construir la imagen Docker
        //             bat 'docker build -t tu_usuario/tu_proyecto .'
        //             // Publicar la imagen en Docker Hub (necesitas haber iniciado sesión antes)
        //             bat 'docker push tu_usuario/tu_proyecto'
        //         }
        //     }
        // }

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
