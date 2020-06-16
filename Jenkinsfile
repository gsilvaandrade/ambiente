<<<<<<< HEAD
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
=======
stage 'Checkout'
 node('slave') {
  deleteDir()
  checkout scm
 }
>>>>>>> dee1f80e8998710d10857836463f8d7751c35865
