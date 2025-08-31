pipeline {
    agent any
    
    tools {
        jdk 'java17'      // must match Global Tool Configuration
        maven 'maven3'    // must match Global Tool Configuration
    }

    stages {
        stage("Cleanup Workspace") {
            steps {
                cleanWs()
            }
        }

        stage("Checkout from SCM"){
            steps {
                git branch: 'main', credentialsId: 'github', url: 'https://github.com/swapnil31121995/DevOps-mega-project-swapnil.git'
            }

        }


        stage("Build the application"){
            steps {
               sh "mvn clean package"
            }

        }

        stage("Test the application"){
            steps {
               sh "mvn test"
            }

        }
    }
    
}