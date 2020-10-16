pipeline {
    agent any
    tools {
        maven 'apache maven 3.6.3'
        jdk 'JDK 8'
    }
    stages {
        stage ('Clean') {
            steps {
                sh 'mvn clean'
            }
        }

        stage ('Build') {
            steps {
                sh 'mvn compile'
            }
        }

        stage ('Install') {
            steps {
                sh 'mvn install'
            }
        }

        stage ('Run Main') {
            steps {
                sh 'mvn exec:java -Dexec.mainClass="learning_java.Main"'
            }
        }

    }
}
