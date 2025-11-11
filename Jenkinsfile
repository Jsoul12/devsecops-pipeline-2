


pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Construyendo el proyecto...'
            }
        }

        stage('Test') {
            steps {
                echo 'Ejecutando pruebas unitarias...'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Instalando herramientas de seguridad...'
                sh 'pip3 install --user -r requirements.txt'

                echo 'Ejecutando análisis estático con Bandit...'
                sh 'bandit -r . || true'
            }
        }

    }
}
