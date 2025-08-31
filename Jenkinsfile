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
    }
}