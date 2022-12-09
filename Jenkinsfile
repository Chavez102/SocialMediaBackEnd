pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'sudo sh ./social-media-spring-main/mvnw clean package -DskipTests'
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
                sh 'java jar .social-media-spring-main/target/*.jar'
            }
        }
    }
}