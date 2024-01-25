pipeline {
    agent { node {label 'agent-1'} }
    enviromnemt {
        USER = "rajkumar"
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