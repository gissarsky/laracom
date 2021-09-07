pipeline {
    agent { label "agent1" }
    stages {
        stage("Deploy") {
            steps {
                sh '''
                    docker-compose up -d --build
                    docker-compose ps --format json
                    cd project && make install
                    '''         
            }
        }
    }
} 