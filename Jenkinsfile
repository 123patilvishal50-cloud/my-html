pipeline{
    agent any

    environment {
        VERCEL_TOKEN = credentials('vercel-token')
    }
    stages{
        stage('Build') {
            steps {
                bat 'npm install'
            }
        }
        stage('test') {
            steps {
                echo "skipping tets"
            }
        }
         stage('deploy') {
            steps {
                bat 'npx vercel --prod --token %VERCEL_TOKEN%'
            }
        }
    }
}