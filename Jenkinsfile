pipeline {
  agent {
    node {
      label 'dev'
    }

  }
  stages {
    stage('git') {
      steps {
        dir(path: '/home/shiyanlou/test_git') {
          git(url: 'https://github.com/Yehnn/test_git.git', branch: 'master', credentialsId: '1df5f28a-e0f5-4053-b782-86606241d773')
        }

      }
    }
    stage('build') {
      steps {
        sh 'sudo -H pip install -r requirements.txt'
      }
    }
    stage('run') {
      steps {
        sh 'python app.py'
      }
    }
  }
}