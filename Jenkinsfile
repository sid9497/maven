pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "my maven"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
               git branch: 'main', url: 'https://github.com/sid9497/maven.git'
                // Run Maven on a Unix agent.
                sh "mvn clean install"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

        }
    }
}
