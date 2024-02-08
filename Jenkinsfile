pipeline {
  agent any
  stages {
    stage('Compile') {
      steps {
        sh './mvnw clean compile'
      }
    }

    stage('Static Analysis') {
      steps {
        sh '''mvnw sonar:sonar \\
  -Dsonar.projectKey=Petclinic \\
  -Dsonar.host.url=http://172.31.11.191:9000 \\
  -Dsonar.token=sqp_f368f7c77a983bb4eb8a6e525d467bc14bc00fad'''
      }
    }

  }
}