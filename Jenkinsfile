pipeline {
    agent any
    stages {
        stage('1. Checkout') {
            steps {
                echo 'Checking out...'
                checkout scm
            }
        }
        stage('2. Validation') {
            steps {
                sh 'ls -lh && echo VALIDATION OK'
            }
        }
        stage('3. Deploy') {
            steps {
                sh 'sudo cp -f index.html /var/www/html/index.html && sudo systemctl reload nginx'
            }
        }
    }
}
