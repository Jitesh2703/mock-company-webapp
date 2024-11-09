pipeline {
  /*
   * TODO: Implement pipeline stages/steps
   *   See documentation: https://www.jenkins.io/doc/book/pipeline/syntax/#stages
   */
    agent any

    stages {
        stage('Build') {
            steps {
                // Build the project using Gradle
                sh './gradlew assemble'
            }
        }

        stage('Test') {
            steps {
                // Run the tests
                sh './gradlew test'
            }
        }
    }

    post {
        success {
            echo 'Build and Test stages completed successfully!'
        }
        failure {
            echo 'Build or Test stage failed!'
        }
    }
}
