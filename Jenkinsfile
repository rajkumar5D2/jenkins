pipeline {
    agent { node {label 'agent-1'} }
    options{
        timeout(time: 1, unit: 'HOURS')
    }
    environment {
        USER = 'rajkumar'
    }
     parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: 'enter something here', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: false, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
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