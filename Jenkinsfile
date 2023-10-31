pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M3"
    }

    stages {
        stage('Checkout') {
            steps {
                // Get some code from a GitHub repository
                git branch: 'main', url:'https://github.com/ShivJulka/hello-world-maven.git'

               
            }
        }
        
      stage('Build') {
            steps {
                // Get some code from a GitHub repository
                echo 'Now running build'
            }
        }
        stage('Unit Tests') {
            steps {
                // Get some code from a GitHub repository
                echo 'Now running tests'
            }
        }
        stage('Package') {
            steps {
                // Get some code from a GitHub repository
                sh "mvn clean compile"
            }
        }
        stage('Deploy to Dev') {
            steps {
                // Get some code from a GitHub repository
                echo "Completed"
            }
        }
        stage('Deploy to Test') {
            steps {
                // Get some code from a GitHub repository
                echo "Completed"
            }
        }
        stage('Deploy to UAT') {
            steps {
                // Get some code from a GitHub repository
                echo "Completed"
            }
        }
        stage('Wait for Business Input') {
            steps {
                script {
                    // Prompt the user for approval to deploy
                    def user_input = input(
                        id: 'user_input',
                        message: 'Do you want to deploy the project?',
                        parameters: [booleanParam(defaultValue: true, description: 'Select to deploy', name: 'Deploy')]
                    )
                    if (user_input) {
                        // Deploy the project
                        echo 'Deploying the project...'
                        // Add your deployment steps here
                    } else {
                        echo 'User canceled the deployment.'
                    }
                }
            }
        }
        stage('Deploy to Production') {
            steps {
                // Get some code from a GitHub repository
                echo "Completed"
            }
        }
        stage('Done') {
            steps {
                // Get some code from a GitHub repository
                echo "Completed"
            }
        }
    }
    
    
}
