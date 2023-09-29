pipeline {
    agent any

    stages {
        stage('Clonar Repositorio') {
            steps {
                script {
                    checkout scm
                }
            }
        }

        stage('Instalar Dependencias') {
            steps {
                sh 'npm install'
            }
        }

        stage('Compilar y Construir') {
            steps {
                script {
                    // Compilar y construir la aplicación Angular
                    sh 'ng build --prod'
                }
            }
        }

        stage('Ejecutar Pruebas Unitarias') {
            steps {
                script {
                    // Ejecutar pruebas unitarias
                    sh 'ng test'
                }
            }
        }

        // stage('Publicar en Docker Hub') {
        //     steps {
        //         script {
        //             // Construir la imagen Docker
        //             sh 'docker build -t tu_usuario/tu_proyecto .'
        //             // Publicar la imagen en Docker Hub (necesitas haber iniciado sesión antes)
        //             sh 'docker push tu_usuario/tu_proyecto'
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
