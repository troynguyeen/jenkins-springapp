pipeline {
    agent any
    tools {
        maven '3.9.1'
    }
    stages {
        stage('Check mvn version') {
            steps {
                sh 'mvn -v'
            }
        }
    }
}