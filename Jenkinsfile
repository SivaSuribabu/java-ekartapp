pipeline {

    agent any

    tools {
        jdk "jdk17"
        maven "maven3"
    }

    environment {
        SONAR_URL = "http://172.17.0.1:9000/"
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

        stage("Unittest"){
            steps{
                sh "mvn package -DskipTests=true"
            }
        }

        stage("Sast"){
            steps{
                withSonarQubeEnv([string(credentialsId: 'sonar-cred', variable: 'SONAR_AUTH_TOKEN')]) {
                    sh 'mvn sonar:sonar -Dsonar.login=$SONAR_AUTH_TOKEN -Dsonar.host.url=${SONAR_URL}'
                }
            }
        }
    }
}