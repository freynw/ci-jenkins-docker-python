pipeline {
    agent { docker { image 'python' } }
    stages {
        stage('Build') {
            steps {
                // Download the code
                checkout scm
                sh 'pwd'
                sh 'whoami'
                sh 'ls -al /usr/bin/*'
                sh 'ls -al /bin/*'
            }
        }
        stage('Test') {
            steps {
                // Run the tests
                sh 'python test_calculator.py'
            }
        }
    }
}
