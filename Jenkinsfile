pipeline{

agent any 

tools{
    java "jdk17"
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