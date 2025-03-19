pipeline {
    agent { label 'Slave' }
    tools {
        maven 'MVN'
    }
    stages {
        stage('Source Code') {
            steps {
                git branch: 'master', url: 'https://github.com/99prerna/QuizApp.git'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean'
                sh 'mvn compile'
                sh 'mvn test'
                sh 'mvn package'
            }
        }
        // stage('Deploy') {
        //     steps {
        //         // Check which user Jenkins is running as
        //         sh 'echo "Urm560037NJ@" | sudo -S cp /Users/nikhiljoshi/Desktop/miniDevOps/QuizApp/target/QuizApp.war /Users/nikhiljoshi/tomcat/webapps'
        //     }
        // }
    }
}
