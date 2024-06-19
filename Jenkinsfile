pipeline {

    agent any

    tools {
        java 'jdk17'
        maven 'maven'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/SivaSuribabu/java-ekartapp.git'
            }
        }
    }
}