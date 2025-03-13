pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                // Compile the .cpp file, build as YOUR_SRN-1
                sh 'g++ -o PES1UG22CS317-1 main/hello.cpp'
                echo 'Build Stage Successful'
            }
        }
        stage('Test') {
            steps {
                // Intentional error: misspelled executable name
                sh './PES1UG22CS317-ONE'  
                echo 'Test Stage Successful'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying Application...'
                sh './PES1UG22CS317-1'
                echo 'Deployment Successful'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
