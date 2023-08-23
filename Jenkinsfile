pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        sh 'pwd'
        sh 'date'
      }
    }

    stage('test') {
      parallel {
        stage('test') {
          steps {
            echo 'test par'
          }
        }

        stage('test par') {
          steps {
            echo 'test par1'
          }
        }

      }
    }

    stage('deploy') {
      steps {
        echo 'deploy'
        sleep 15
      }
    }

  }
}