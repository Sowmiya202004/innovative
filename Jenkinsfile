pipeline {
    agent any

    tools {
        jdk 'JDK'
        maven 'MAVEN'
    }

    stages {

        stage('Build') {
            steps {
                bat 'mvn clean package'
            }
        }

        stage('Deploy Website') {
            steps {
                echo 'Publishing website'
            }
        }

    }

    post {
        success {
            publishHTML([
                reportDir: '.',
                reportFiles: 'CourseApplet.html',
                reportName: 'Course Website'
            ])
        }
    }
}
