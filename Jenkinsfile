pipeline {
    agent { node {label 'agent-1'} }
    options{
        timeout(time: 1, unit: 'HOURS')
    }
    environment {
        USER = 'rajkumar'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building-111..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing-222..'
                sh 'printenv'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
        
    }
    post{
        always{
            echo "i'll run always"
        }
        
    }
}