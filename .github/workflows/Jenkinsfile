pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'git clone https://github.com/Philw10/DevOps-Course-Workshop-Module-07-Learners.git'
                sh 'dotnet build'
                dir ('DotnetTemplate.web') {
                    sh 'npm install'
                    sh 'npm run build'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}