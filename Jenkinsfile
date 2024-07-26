pipeline {
  agent any
  stages {
    stage('From SCM') {
      steps {
        git(url: 'https://github.com/venky1509/nts26_repo3.git', branch: 'main', credentialsId: '9c76ac2d-4620-4cb7-92e3-656992ad4c23', poll: true)
      }
    }

    stage('Terraforminit') {
      steps {
        bat(script: 'terraform init', label: 'init')
      }
    }

    stage('deploy') {
      agent any
      steps {
        bat(script: 'echo "Deploy to prod"', label: 'deploy')
      }
    }

  }
}