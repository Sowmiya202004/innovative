pipeline {
    agent any

    tools {
        maven 'MAVEN'
    }

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Application Built and Deployed Successfully'
            }
        }

    }
}
