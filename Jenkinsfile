pipeline {
    agent {
        label ''
    }

    stages {

        stage('Checkout') {
            steps {
                echo 'Stage 1: Checking out Python Build Test project...'
                git branch: 'main',
                    url: 'https://github.com/Jeevanantham74/python-build-test.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                echo 'Stage 2: Installing dependencies...'
                bat 'py -m pip install -r requirements.txt'
            }
        }

        stage('Run Unit Tests') {
            steps {
                echo 'Stage 3: Running unit tests...'
                bat 'py -m pytest test_app.py -v'
            }
        }
    }
}