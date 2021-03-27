pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Hello"
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/rjonala/docker-hello-world-spring-boot.git']]])
            }
        }
    }
}
