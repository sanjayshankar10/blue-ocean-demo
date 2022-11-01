pipeline {
  agent any
  stages {
    stage('Install apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('Fetch code') {
      steps {
        git(url: 'https://github.com/sanjayshankar10/blue-ocean-demo.git', branch: 'main')
      }
    }

    stage('deploy app') {
      steps {
        sh 'sudo cp -R . /var/www/html/'
      }
    }

  }
}