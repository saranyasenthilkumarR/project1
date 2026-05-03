pipeline {
    agent any

       stages {
       stage('Build Docker Image') {
            steps {
              sh "docker build -t myapp:01 ."
            }
        }
     stage ('docker run') {
       steps{
         sh "docker run --rm myapp:01"
       }
     }
    }
  

    post {
    always {
        sh 'docker system prune -f'
        }
    }
}
