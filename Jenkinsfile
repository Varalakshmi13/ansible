//firs i want to do a dry run

pipeline {
  agent any

  options {
    ansiColor('xterm')
  }

  stages {
    stage('Do  dry run') {
      steps {
        sh '''
            export ALLOW_WORLD_READABLE_TMPFILES=True
            ansible-playbook roboshop.yml -e HOST=localhost -e role_name=frontend -C
        ''' // allow command is to resolve the
      }

    }
  }



  }