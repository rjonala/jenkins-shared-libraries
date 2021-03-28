pipeline {
    agent {
        docker { image 'docker' }
    }
    stages {
        stage("Build") {
            steps {
                echo "Hello"
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/rjonala/docker-hello-world-spring-boot.git']]])
                sh 'sudo docker build .'
            }
        }
    }
}
