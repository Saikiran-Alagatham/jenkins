pipeline {

    agent any

    environment{
        temp = "abc"
    }

  stages {
     
        stage('Master Node') 
        {
                    agent
                    {
                        label 'MASTER'
                    }
                    steps {
                        sh 'echo Running on master'
                    }
            }
            stage('Agent Node') 
            {
                    agent
                    {
                        label 'Java'
                    }
                    steps {
                        sh 'echo Running on Agent/workstation'
                    }
            }

            stage("Environmentals varibles example"){
                environment{
                        temp = "def"
                    }
                    steps{
                        sh 'echo ${temp}'
                    }
            }

            stage("Input example"){
                input{
                    message ' Approve or not'
                    ok ' Approve'
                }
                    steps{
                        sh 'echo Process Approved'
                    }
            }
    }

    post{
        always{
            sh 'echo Example of post section'
        }
    }

}