pipeline {
    agent any
    stages {
        stage('Development') {
            steps {
                echo "Building the application with Maven Wrapper..."
                sh './mvnw clean install'
                echo "Build completed successfully!"
            }
        }

        stage('Testing') {
            steps {
                echo "Running tests with Maven Wrapper..."
                sh './mvnw test'
                echo "Tests completed successfully!"
            }
        }

        stage('Production') {
            steps {
                echo "Deploying to production environment..."
                // Tambahkan skrip deployment di sini jika ada
                echo "Production deployment completed!"
            }
        }
    }
    post {
        success {
            echo "Pipeline completed successfully!"
        }
        failure {
            echo "Pipeline failed. Please check the logs."
        }
    }
}
