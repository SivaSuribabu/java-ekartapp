pipeline {

    agent any

    tools {
        jdk "jdk17"
        maven "maven3"
    }

    stages{
        stage("Checkout"){
            steps{ checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/SivaSuribabu/java-ekartapp.git']])
            }
        }

        stage("Compile"){
            steps{
                sh "mvn compile"
            }
        }
    }
}