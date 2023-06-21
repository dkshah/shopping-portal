pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the build the app job'
        sh 'npm install'
      }
    }

    stage('test') {
      steps {
        echo 'this is the test app job'
        sh 'npm test'
      }
    }

    stage('package') {
      steps {
        echo 'this is the package job'
        sh 'npm run package'
      }
    }

    stage('Archive') {
      steps {
        archiveArtifacts '**/distribution/*.zip'
      }
    }

  }
  tools {
    nodejs 'nodejs'
  }
  post {
    always {
      echo 'Hello This is my first pipeline...'
    }

  }
}