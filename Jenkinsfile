pipeline {
    agent { node {label 'agent-1'} }

    stages {
        stage('Build') {
            steps {
                echo 'Building-111..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing-222..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying-333....'
            }
        }
        
    }
    post{
        always{
            echo "i'll run always"
        }
        
    }
}