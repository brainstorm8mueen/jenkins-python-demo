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
                sh 'python3 -m pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                echo "Running tests..."    
                sh 'python3 -m pytest'
            }
        }

        stage('Build') {
            steps {
                echo "Building the application..."
                sh 'python3 app.py'
            }
        }
    }
}
