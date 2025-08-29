/*pipeline {
    agent any
    triggers {
        //pollSCM('H/2 * * * *')  
        // check every 2 minutes for changes  
         githubPush()
    }
    stages {
        stage('Build') {
            steps {
                echo "Hello from my own GitHub repo!"
            }
        }
    }
}
*/
pipeline {
    agent { label 'windows-node' }  // runs on your Windows agent

    triggers {
        pollSCM('* * * * *')  // check GitHub changes every 1 minutes
    }

    stages {
        stage('Build') {
            steps {
                echo "Build stage running on Windows agent"
                //bat 'ver'  // shows Windows version
            }
        }
        stage('Test') {
            steps {
                echo "Test stage running on Windows agent"
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploy stage running on Windows agent"
            }
        }
    }
}

