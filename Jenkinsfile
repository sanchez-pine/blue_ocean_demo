pipeline {
  agent any
  stages {
    stage('checkoutGit') {
      steps {
        git(url: 'https://github.com/sanchez-pine/blue_ocean_demo.git', branch: 'main')
      }
    }

    stage('build') {
      steps {
        echo 'This is build'
      }
    }

    stage('Deploy') {
      parallel {
        stage('Deploy to Dev 1') {
          steps {
            sleep 30
            echo 'finished'
          }
        }

        stage('Deploy to Dev 2') {
          steps {
            sleep 20
            echo 'completed'
          }
        }

      }
    }

    stage('test') {
      steps {
        echo 'testing...'
      }
    }

  }
}