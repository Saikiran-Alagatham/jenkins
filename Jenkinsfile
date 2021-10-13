pipeline {

    agent any

  stages {
     
   stage('Master Node') {
        agent
      {
          label 'MASTER'
      }
      steps {
        sh 'echo Running on master'
      }
    }
   stage('Agent Node') {
       agent
      {
          label 'Java'
      }
     steps {
        sh 'echo Running on Agent/workstation'
      }
    }
    }

    post{
        always{
            sh 'echo Example of post section'
        }
    }

}