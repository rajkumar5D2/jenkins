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
                      }
        }
        stage('Example') {
        input {
            message "Should we continue?"
            ok "Yes, we should."
            submitter "alice,bob"
            parameters {
                string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
            }
        }
             steps {
                echo "Hello, ${PERSON}, nice to meet you."
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