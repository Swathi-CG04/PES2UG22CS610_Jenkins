pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o hello_exec main/hello.cpp'
                    echo "Build Stage Completed "
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './hello_exec'
                    echo "Test Stage Completed "
                }
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying the application... "
                echo "Deployment Successful "
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed '
        }
        success {
            echo 'Pipeline executed successfully '
        }
    }
}
