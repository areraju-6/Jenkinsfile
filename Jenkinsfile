properties([pipelineTriggers([githubPush()])])

pipeline {
    agent {label "slave1"}
    stages {
        stage ("clone") {
            steps {
                git url: 'https://github.com/areraju-6/Jenkinsfile.git'
            }
        }
        stage ("build") {
            steps {
                sh "mvn clean install"
            }
        }
    }
}
