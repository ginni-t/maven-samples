pipeline {
    agent any

    tools {
        maven 'Maven3'
        jdk 'JDK8'
    }

    stages {
        stage('check out') {
            steps {
                git(url: 'https://github.com/ginni-t/maven-samples.git', branch: 'master')
            }
        }

        stage('run') {
            steps {
                sh 'mvn clean test verify'
            }
        }
    }
}
