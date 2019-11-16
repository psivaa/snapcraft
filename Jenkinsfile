pipeline {
  agent {
    docker {
      image 'ubuntu'
    }

  }
  stages {
    stage('Build') {
      steps {
        echo 'Building'
      }
    }
    stage('Test') {
      steps {
        sh 'ping -2 google.com'
      }
    }
    stage('deploy') {
      steps {
        node(label: 'para')
      }
    }
  }
}