pipeline {
  agent any
  stages {
    stage('fetching the code') {
      steps {
        git(url: 'https://github.com/Danielkevin25/jenkins-blueocean.git', branch: 'main', poll: true)
      }
    }

    stage('installing apache') {
      steps {
        sh 'sudo apt install apache2 -y'
      }
    }

    stage('deploying the code') {
      steps {
        sh 'sudo cp -R * /var/www/html/'
      }
    }

  }
}