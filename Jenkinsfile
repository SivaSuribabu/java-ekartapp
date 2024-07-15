pipeline{

    agent any 

    tools{
    java "jdk"
    maven "maven"   
    }

    stages{
        stage('Checkout'){
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/SivaSuribabu/java-ekartapp.git']])
            }
        }

        stage('Compile'){
            steps{
                sh 'mvn compile'
            }
        }
    }
}