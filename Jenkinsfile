pipeline {
    agent any
    tools {
        maven '3.9.1'
    }
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean package -B -DskipTests'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml' 
                }
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying...'
            }
        }
    }
}
