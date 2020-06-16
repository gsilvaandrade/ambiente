 pipeline {
   {
        stage('Build Docker Image') {
            steps {
              deleteDir()
			  checkout scm
            }
        }

     
    }

    post {
        always {
            deleteDir()
        }
    }
}
