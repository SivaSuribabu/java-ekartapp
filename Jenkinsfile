pipeline{

    tools{
        java 'jdk17'
        maven 'maven'
    }

    stages{
        stage{
            steps('checkout'){
                git branch: 'main', url: 'https://github.com/SivaSuribabu/java-ekartapp.git'
            }
        }
    }
}