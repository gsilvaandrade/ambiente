
pipeline {
   
    stages {

        stage('Build Docker Image') {
            steps {
                script {
                    def dockerfile = readFile 'Dockerfile'
                    writeFile file: "Dockerfile-1.0", text: dockerfile
                }
                sh "docker build -t -f Dockerfile-1.0 ."
                sh "docker push http://localhost:8081/"
            }
        }

    }

    post {
        always {
            deleteDir()
        }
    }
}