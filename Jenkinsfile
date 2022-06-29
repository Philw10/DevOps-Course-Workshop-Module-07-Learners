pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                bat 'git clone https://github.com/Philw10/DevOps-Course-Workshop-Module-07-Learners.git'
                bat 'dotnet build'
                dir ('DotnetTemplate.web') {
                    bat 'npm install'
                    bat 'npm run build'
                }
            }
        }
        stage('Test') {
            steps {
                bat 'dotnet test'
                dir ('DotnetTemplate.web') {
                    bat 'npm t'
                    bat 'npm run lint'
                }
            }
        }
        
    }
}