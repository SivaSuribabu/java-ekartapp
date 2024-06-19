pipeline {
    agent any

    tools {
        jdk 'jdk17'
        maven 'maven'
    }

    stages {
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], userRemoteConfigs: [[url: 'https://github.com/SivaSuribabu/java-ekartapp.git']]])
            }
        }

        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
    }

    post {
        always {
            echo 'Pipeline completed'
        }
        success {
            echo 'Pipeline succeeded'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
