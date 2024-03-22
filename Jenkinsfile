pipeline {
    agent any
    
    stages {
        stage('Checkout') {
            steps {
                // Checkout the code from the Git repository
                git 'https://github.com/atulbarge1989/hello-world.git'
            }
        }
        
        stage('Build') {
            steps {
                // Clean and install Maven dependencies
                sh 'mvn clean install'
            }
        }
    }
    
    post {
        always {
            // Clean up workspace
            cleanWs()
        }
    }
}
