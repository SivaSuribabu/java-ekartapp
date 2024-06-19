pipeline {

    agent any

    tools {
        Java 'jdk17'
        Maven 'maven'
    }

    stages {
        stage('Checkout') {
            steps {
                git branch: 'main', url: 'https://github.com/SivaSuribabu/java-ekartapp.git'
            }
        }


        stage('Compile') {
            steps {
                sh 'mvn compile'
            }
        }
    }
}