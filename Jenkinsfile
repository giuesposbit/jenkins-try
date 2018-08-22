pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                sh 'echo "Build step1"'
                sh 'echo "Build step2"'
            }
        }
        stage('Test') {
            steps {
                sh 'echo "Test step1"'
                sh 'echo "Test step2"'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo "Deploy step1"'
                sh 'echo "Deploy step2"'
            }
        }
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
