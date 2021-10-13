pipeline {

    agent any

  stages {
      agent
      {
          label 'MASTER'
      }
   stage('Master Node') {
      steps {
        sh 'echo Hello'
      }
    }
   stage('Agent Node') {
       agent
      {
          label 'MASTER'
      }
     steps {
        sh 'echo Hello'
      }
    }
    }

}