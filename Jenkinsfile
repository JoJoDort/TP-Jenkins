pipeline {
    agent any

    stages {
        stage('Example') {
            steps {
                echo "Start"

                retry(2) {
                    bat 'echo Retry block running'
                }

                timeout(time: 1, unit: 'MINUTES') {
                    bat 'echo Timeout block running'
                }

                bat 'echo Finish'
            }
        }
    }
}
