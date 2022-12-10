pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                
                 dir('social-media-spring-main') {
//                   sh "pwd"
                sh 'ls'
//                   sh 'mvn -N wrapper:wrapper -Dmaven=3.2.5'
                  sh 'sudo sh ./mvnw clean package -DskipTests'
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
                sh 'ls'


                dir('social-media-spring-main') { 
                  sh 'ls' 
                  //sh 'sudo sh ./mvnw clean package -DskipTests'
 //                 sh 'BUILD_ID=dontKillMe nohup java -jar ./target/*.jar &'
                     sh 'java -jar ./target/*.jar'
//                      sh 'java -jar ./target/*.jar'
                    
                  
                 }

                 
                
            }
        }
    }
}
