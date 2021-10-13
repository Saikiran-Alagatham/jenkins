pipeline {

    agent any

  stages {
     
   stage('Master Node') {
        agent
      {
          label 'MASTER'
      }
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