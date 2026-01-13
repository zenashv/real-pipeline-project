pipeline{
  agent any

  stages{

    stage('Checkout Code'){
      steps{
        echo 'Pulling Code from github'
        checkout scm
      }
    }
    stage('Build') {
      steps {
        echo 'Building the application'
        sh 'ls -l'
      }
    }

    stage('Test') {
      steps {
        echo 'Testing the application'
        sh 'bash test.sh'
      }
    }


    stage('Deploy') {
      steps {
        echo 'Deploying the application'
        sh 'echo "Website CI pipeline executed succesfully"'
      }
    }
  }

  post {
   success {
     echo 'CI pipeline Success'
   }
   failure {
     echo 'CI pipeline Failure'
  }
}
