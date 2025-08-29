pipeline {
    agent any
    triggers {
        pollSCM('H/2 * * * *')  
        // check every 2 minutes for changes
    }
    stages {
        stage('Build') {
            steps {
                echo "Hello from my own GitHub repo!"
            }
        }
    }
}
