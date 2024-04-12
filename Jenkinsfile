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
    }
}
