pipeline {
  agent any

  options {
    ansiColor('xterm')
  }

  environment {
    SSH = credentials('SSH')
  }

  stages {

    stage('Check Ansible Style Checks') {
      when { branch pattern: "ROB-.*", comparator: "REGEXP"}
      steps {
       echo "Ansible Style Checks"
        // We will find the right tool.
      }
    }

    stage('Run Ansible in Sandbox Environment') {
      when { branch pattern: "PR-.*", comparator: "REGEXP"}
      steps {
        sh '''
          ansible-playbook roboshop-check.yml -e role_name=frontend -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -e ENV=sandbox -e CHECK_MODE=true
        '''
      }
    }



    stage('Promote Code to PROD Branch') {
      when { branch 'main' }
      steps {
        sh 'env'
        sh 'echo MAIN'
      }
    }


  }

// Here we are hardcoding role_name as frontend as for demo purpose, But we need to understand which role has been really modified and we need to parse that
// role name, We can get that infor from git commands, Here is the example.    git diff HEAD@{1} --name-only | grep roles | awk -F / '{print $2}'
//    stage('Do a Dry Run') {
//      steps {
//        sh '''
//          env
//          #ansible-playbook roboshop-check.yml -e role_name=frontend -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -e ENV=sandbox -e CHECK_MODE=true
//        '''
//      }
//    }

}
