pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building PES2UG22CS251...'
                sh 'g++ -o my_program my_program.cpp' // Compile C++ file
            }
        }
        
        stage('Test') {
            steps {
                echo 'Running tests...'
                sh './my_program' // Print output of C++ file
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the application...'
                sh 'scp my_program user@server:/deploy/path/' // Example deploy command
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline executed successfully!'
        }
    }
}
