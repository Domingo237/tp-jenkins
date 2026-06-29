pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                echo 'Projet récupéré depuis GitHub'
            }
        }

        stage('Build') {
            steps {
                bat 'dir'
            }
        }

        stage('Test') {
            steps {
                bat 'if exist index.html (echo index.html trouvé) else (exit 1)'
            }
        }

        stage('Archive') {
            steps {
                archiveArtifacts artifacts: 'index.html', fingerprint: true
            }
        }

        stage('Deploy') {
            steps {
                echo 'Déploiement simulé'
            }
        }
    }

    post {
        success {
            echo 'Pipeline terminé avec succès.'
        }

        failure {
            echo 'Le pipeline a échoué.'
        }
    }
}
