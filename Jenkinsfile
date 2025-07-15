pipeline {
    agent any

    stages {
        stage('Clone Code') {
            steps {
                git branch: 'main', url: 'https://github.com/Mohammedriyaz123/snake-game'
            }
        }

        stage('Build') {
            steps {
                echo 'No build step needed for static files.'
            }
        }

        stage('Test') {
            steps {
                echo 'No tests for static game, skipping.'
            }
        }

        stage('Deploy') {
            steps {
                sh '''
                    echo "Deploying snake game..."
                    sudo rm -rf /var/www/html/*
                    sudo cp -r * /var/www/html/
                '''
            }
        }
    }
}
