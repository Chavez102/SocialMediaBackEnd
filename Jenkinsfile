pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'ls'
                sh 'cd social-media-spring-main'
                sh 'ls'
                sh 'mvn -N wrapper:wrapper -Dmaven=3.2.5'

                sh 'sudo sh ./mvnw clean package -DskipTests'
                
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
