pipeline {
  agent any

  parameters {
    string(name: 'USERNAME', defaultValue: 'admin', description: 'Linux user to create')
  }

  stages {
    stage('Run Ansible') {
      steps {
        sh '''
          cd ansible
          ansible-playbook -i inventory site.yml -e username=${USERNAME}
        '''
      }
    }
  }
}
