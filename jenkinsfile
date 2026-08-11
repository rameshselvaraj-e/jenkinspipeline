pipeline {
  agent any
  stages {
    stage('Checkout') {
      steps {
        //git 'https://github.com/rameshselvaraj-e/jenkinspipeline'
        echo 'test'
      }
    }
    stage('Run Ansible') {
      steps {
        sshagent(['ansible-jenkins']) {
            sh 'ansible-playbook -i test.txt test.yml'
            //sh 'ssh -o StrictHostKeyChecking=no itadmin@10.0.10.10 "echo Connected from Jenkins!"'
        }  
      }
    }
  }
}
