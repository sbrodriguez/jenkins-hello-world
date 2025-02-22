pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M398"
    }
    
    stages {
        stage ('Echo Version') {
            steps {
                sh 'echo Print Maven Version'
                sh 'mvn -version'
            }
        }
        
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                //git branch: 'main', url: 'https://github.com/sbrodriguez/jenkins-hello-world'

                // Run Maven pkg CMD.
                sh "mvn clean package -DskipTests=true"
                }
            }
        
        stage('Unit Test') {
            steps {
                sh "mvn test"
            }   
        }
    }
}
