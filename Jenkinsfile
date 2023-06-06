pipeline {
    agent {
        label "demoAgent"
    }
    stages {
        stage('git') {
            steps {
                git branch: 'main', url: 'https://github.com/jjddhh/jenkins-demo.git'
            }
        }        
        stage('mvn') {
            steps {
                sh "mvn -Dmaven.test.failure.ignore=true clean test"
            }
        }
    }
}
