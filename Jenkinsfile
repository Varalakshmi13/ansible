//firs i want to do a dry run

pipeline {
  agent any

  stages {
    stage('Do  dry run') {
      steps {
        sh '''
            ansible-playbook roboshop.yml -e HOST=localhost -e role_name=frontend
        '''
      }

    }
  }



  }