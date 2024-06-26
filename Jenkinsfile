pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'This is the Build job'
        sh 'npm install'
      }
    }

    stage('Test') {
      steps {
        echo 'This is the Test job'
        sh 'npm test'
      }
    }

    stage('Package') {
      steps {
        echo 'This is the Package job'
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
      echo 'This pipeline has completed...'
    }

  }
}