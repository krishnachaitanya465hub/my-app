pipeline {
    agent any
    stages {
        stage('---clean---') {
            steps {
                sh "mvn clean"
            }
        }
        stage('--compile--') {
            steps {
                sh "mvn compile"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package"
            }
        }
        stage('--deploy--') {
            steps {
                sh "cp /root/.jenkins/workspace/pipeline-3/target/my-app-1.0-SNAPSHOT.jar /opt/apache-tomcat-8.5.35/webapps/"
            }
        }
    }
}
