pipeline {

    agent any

    stages {

        stage('Checkout Code') {
            steps {
                echo 'Checking out code from Github...'
                checkout scm
            }
        }

        stage('Install Dependencies') {
            steps {
                echo " Installing dependencies..."
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                echo "Running tests..."    
                sh 'pytest'
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
                sh 'python app.py'
            }
        }
    }
}