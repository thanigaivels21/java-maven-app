pipeline{
    agent any

    stages{
        stage('SCM Checkout'){
            steps{
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'Git_Token', url: 'https://github.com/getyourdurga/java-maven-app.git']])
            }
            
        }
        stage('maven-build'){
            steps{
                sh 'mvn clean install'
            }
        }
    }

}