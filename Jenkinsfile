pipeline {
    agent any
    tools {
        nodejs 'nodejs'
    }

    stages {
        stage('Clone Code') {
            steps {
                echo 'Cloning code...'
                git (url: 'https://github.com/tin3ga/gallery', branch: 'master')
                
            }
        }
        stage('Install dependencies') {
            steps {
                echo 'Installing dependencies...'
                sh 'npm install'
            }
        }
         stage('Test') {
            steps {
                echo 'Running tests...'
                sh 'npm test'
            }
        }
         stage('Deploy') {
            steps {
                echo 'Deploying...'
                sh 'curl https://api.render.com/deploy/srv-cod9r88l5elc73fjjiug?key=MHsesUhfg5A'
            }
        }
    }
}
