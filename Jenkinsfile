pipeline {
    agent any
    stages {
        stage('Development') {
            steps {
               echo("Start Build...")
               sh("./mvnw clean compile this file")
               echo("Finish Build")
            }
        }

        stage('Deployment') {
            steps {
               echo("start build...")
               sh("./mvnw test")
               echo("Finish Build")
            }
        }

        stage('Production') {
            steps {
                echo("Productionnnnn!!!!!")
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
