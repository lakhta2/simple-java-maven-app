pipeline {
    agent any
    tools {
        maven 'maven-3.9'
    }
    stages {
        stage('Checkout') {
            steps {
                git branch: 'master', url: 'https://github.com/lakhta2/simple-java-maven-app'
            }
        }

        stage('Build + Build2'){
        parallel{
        stage('Build') {
            steps {
                // Замените на команду сборки вашего проекта, например, sh 'mvn clean package'
                echo 'Сборка проекта...'
                sh 'ls -la'
                sh 'mvn clean package'
            }
            }
        stage('Build2') {
            steps {
                echo 'Sborka 2 started...'
                echo 'Sborka 2 working...'
                echo 'Sborka 2 ended...'
            }
        }
        }
        }
    }
}
