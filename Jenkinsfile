@Library('Shared') _

pipeline {
    agent any

    stages {
        
        stage('Clone') {
            steps {
                clone("https://github.com/pmshrik/django-notes-app.git", "main")
            }
        }

        stage('Build Docker') {
            steps { dockerBuild() }
        }

        stage('Up Services') {
            steps { dockerUp() }
        }

        stage('Login DockerHub') {
            steps { dockerLogin() }
        }


    }
}
